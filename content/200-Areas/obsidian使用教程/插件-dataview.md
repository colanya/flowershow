---
aliases:
  - 插件-dataview
category: 视频
state: 已完成
tags:
  - obsidian
  - plugin
  - later
from:
  - bilibili
  - pkmer
url:
  - https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/dataview/dataview%E8%AF%AD%E6%B3%95%E5%AE%9E%E6%88%98/dataview-%E4%BB%BB%E5%8A%A1%E8%BF%9B%E9%98%B6%E6%9F%A5%E8%AF%A2%E7%A4%BA%E4%BE%8B/
  - https://zhuanlan.zhihu.com/p/614881764
stars: 
created: "2024-05-06 15:13"
updated: "2024-05-28 12:28"
dg-publish: 
media: https://www.bilibili.com/video/BV1Hu4y1w7tL
---
## 基本用法
- [00:02:34](https://www.bilibili.com/vdeo/BV1Hu4y1w7tL?t=154.034076#t=02:34.03) 添加元数据
	- 快捷键**Ctrl+;** 创建文档属性
	- 可添加type、location、Project、tags等标签
	- [00:04:32](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=272#t=04:32) 用`::`在文章内添加元数据，用()括起来可以隐藏属性名和冒号
- [00:05:45](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=345.559575#t=05:45.56) 筛选笔记
	- [00:06:04](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=364.944805#t=06:04.94) 插入代码块，代码类型写dataview 
	- [00:06:40](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=400.309284#t=06:40.31) 视图：list、table、task、calendar
	- [00:07:16](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=436.384358#t=07:16.38) from语句：划定筛选范围
		- `#tag`筛选标签
		- `"dict"`筛选文件夹
		- `from ""`筛选所有笔记
	- [00:08:08](https://www.bilibili.com/vide/BV1Hu4y1w7tL?t=488.63213#t=08:08.63) where语句：划定筛选条件
		- `where contains(project, "Project A")` 筛选包含Project属性为Project A的文件
	- [00:08:30](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=510.287063#t=08:30.29) sort语句：排序
		- `sort file.name asc/desc`按照文件名升序/降序排列
- [00:09:36](https://www.bilibili.com/vieo/BV1Hu4y1w7tL?t=576.889154#t=09:36.89) list视图
	- [00:10:47](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=647.871292#t=10:47.87) 效果：将笔记标题列举出来
	- [00:11:49](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=709.575845#t=11:49.58) and链接where中的多个筛选条件
	- [00:12:10](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=730.107234#t=12:10.11) 在list后面输入属性名，可以在列表中显示属性值，但list只能显示一种属性
- [00:12:42](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=762.31266#t=12:42.31) table视图
	- [00:13:01](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=781.755697#t=13:01.76) 格式：`table location，tags` 用逗号分隔表头
	- [00:17:48](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1068.954024#t=17:48.95)定义表头的别称
		- `table date as "日期", summary as "摘要"`用as来提出显示名称
- [00:18:35](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1115.162494#t=18:35.16) task视图 
	- [00:20:07](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1207.830498#t=20:07.83) 功能：列出筛选文件中的任务
	- [00:20:53](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1253.295323#t=20:53.30) `!completed`表示筛选出未完成的任务
- [00:21:32](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1292.50545#t=21:32.51) calendar视图
	- [00:22:18](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1338.999999#t=22:19.00) 统计每天创建、修改的笔记数量
- [00:23:32](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1412.447552#t=23:32.45) 使用场景实例
	- [00:27:40](https://www.bilibili.com/video/BV1Hu4y1w7tL?t=1660.724483#t=27:40.72) 统计今年看过的所有书，电影等
## task用法
### 列出未完成的任务

```
TASK
FROM "10 Example Data/assignments"
WHERE !completed
```

### 将任务按文件分组

```
TASK
FROM "10 Example Data/assignments"
GROUP BY file.link
```

### 包含 #later 标签的文件

```
TASK
FROM "10 Example Data/assignments"
WHERE contains(tags, "#later")
```

### 列出有截止日期的任务
> 在这一篇中我们讲了如何给任务添加元数据，简单的来说就是在任务的末尾加上`[duedate:: 2022-09-09]`或者`[contact:: Petro]`等等，你想添加什么元数据都可以，只需要记住把他们放在方括号内。下面查询的任务已经加上了 duedate 的内联字段，因此如果你的任务没有加 duedate 的话，下面这段代码对你的库不起效果。

```
TASK
FROM "10 Example Data/assignments"
WHERE duedate
```

### 根据完成时间排序已完成的任务
> 正常来说任务的完成时间是不会被记录的。如果想要检索任务的完成时间，我们也需要自己向任务添加元数据。Dataview 提供了一个自动添加的功能，可以当你在 Dataview 视图中选中任务的时候自动将任务的完成日期添加到这个任务的 completion 元素据中。你可以在 Dataview 的设置最下面的 Task Settings 中找到一个 Automatic Task Completion Tracking 设置，打开即可启用。

> ⚠ 强调! 只有在 Dataview 的任务查询框框中选中了任务，dataview 才可以自动添加这个元数据到这个任务。

```
TASK
FROM "10 Example Data/assignments"
WHERE completed
SORT completion
```