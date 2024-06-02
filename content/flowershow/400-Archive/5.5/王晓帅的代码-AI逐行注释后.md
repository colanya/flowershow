---
aliases: 
category: 
state: 
tags: 
from: 
url: 
stars: 
created: "2024-05-05 13:14"
updated: "2024-05-28 12:28"
dg-publish: 
---

```python
import pprint  # 导入pprint模块，用于美化输出
import torch  # 导入PyTorch框架
from tensorboardX import SummaryWriter  # 导入SummaryWriter，用于TensorBoard可视化
from psdet.utils.config import get_config  # 导入获取配置文件的函数
from psdet.utils.common import get_logger, set_random_seed  # 导入获取日志器和设置随机种子的函数

from psdet.utils import dist  # 导入分布式训练相关的模块
from psdet.models import model_fn_decorator  # 导入模型功能装饰器
from psdet.models.builder import build_model  # 导入构建模型的函数
from psdet.datasets.builder import build_dataloader  # 导入构建数据加载器的函数

from train_utils.optimization import build_optimizer, build_scheduler  # 导入构建优化器和调度器的函数
from train_utils.train_utils import train_model  # 导入训练模型的函数

def main():
    cfg = get_config()  # 从配置文件中获取配置信息
    logger = get_logger(cfg.log_dir, cfg.tag)  # 初始化日志器
    logger.info(pprint.pformat(cfg))  # 将配置信息格式化后输出到日志
    
    if cfg.launcher == 'none':  # 判断是否使用分布式训练
        dist_train = False
    else:
        cfg.batch_size, cfg.local_rank = dist.init_dist_pytorch(  # 初始化PyTorch分布式训练环境
            cfg.batch_size, cfg.local_rank, backend='nccl'
        )
        cfg.data.train.batch_size = cfg.batch_size  # 更新训练数据的批量大小
        dist_train = True

    set_random_seed(cfg['random_seed'])  # 设置随机种子，保证实验的可重复性

    if dist_train:  # 如果是分布式训练，计算总的批量大小
        total_gpus = dist.get_world_size()
        logger.info('total_batch_size: %d' % (total_gpus * cfg.batch_size))

    tb_log = SummaryWriter(log_dir=str(cfg.log_dir)) if cfg.local_rank == 0 else None  # 初始化TensorBoard日志记录器

    train_set, train_loader, train_sampler = build_dataloader(  # 构建数据加载器
            cfg.data.train, dist=dist_train, training=True, logger=logger)

    model = build_model(cfg.model)  # 构建模型
    if cfg.get('sync_bn', False):  # 如果配置中启用了同步批量归一化
        model = torch.nn.SyncBatchNorm.convert_sync_batchnorm(model)
    model.cuda()  # 将模型转移到CUDA设备上
    
    optimizer = build_optimizer(model, cfg.optimization)  # 构建优化器

    start_epoch = it = 0
    last_epoch = -1
    if cfg.ckpt is not None:  # 如果有指定检查点文件，从检查点恢复模型和优化器状态
        it, start_epoch = model.load_params_with_optimizer(cfg.ckpt, to_cpu=dist, optimizer=optimizer, logger=logger)
        last_epoch = start_epoch + 1

    model.train()  # 将模型设置为训练模式
    if dist_train:  # 如果是分布式训练，包装模型以支持分布式
        model = torch.nn.parallel.DistributedDataParallel(
                model, device_ids=[cfg.local_rank % torch.cuda.device_count()])
    logger.info(model)

    total_iters_each_epoch = len(train_loader)  # 计算每个epoch的迭代次数
    lr_scheduler, lr_warmup_scheduler = build_scheduler(  # 构建学习率调度器
        optimizer, total_iters_each_epoch=total_iters_each_epoch, total_epochs=cfg.epochs,
        last_epoch=last_epoch, optim_cfg=cfg.optimization
    )

    # -----------------------开始训练---------------------------
    logger.info('*'*20 + 'Start training' +'*'*20)
    
    train_model(  # 训练模型
        model,
        optimizer,
        train_loader,
        model_func=model_fn_decorator(),
        lr_scheduler=lr_scheduler,
        optim_cfg=cfg.optimization,
        start_epoch=start_epoch,
        total_epochs=cfg.epochs,
        start_iter=it,
        rank=cfg.local_rank,
        tb_log=tb_log,
        ckpt_save_dir=cfg.model_dir,
        train_sampler=train_sampler,
        lr_warmup_scheduler=lr_warmup_scheduler,
        ckpt_save_interval=cfg.ckpt_save_interval,
        max_ckpt_save_num=cfg.max_ckpt_save_num,
        merge_all_iters_to_one_epoch=False
    )
    logger.info('*'*20 + 'End training' +'*'*20)
    

if __name__ == '__main__':
    main()
```