---
aliases:
  - 插件-excalidraw
category: 知识
state: 已完成
tags:
  - excalidraw
  - obsidian
  - plugin
from: zhihu
url: https://zhuanlan.zhihu.com/p/658366428
stars: 
created: "2024-05-06 15:13"
updated: "2024-05-28 12:28"
dg-publish: 
---
花了几天时间，从头看了一下Zsolt的油管各版本更新，写了个obsidian-Excalidraw的功能手册，尽量详细，后续更新也会补充在文章下面

## **1.新建excalidraw绘图**

完成插件安装后，可以在任一文件夹点击**鼠标右键-新建excalidraw绘图**，或者点击**最左侧excalidraw图标**，新建绘图

---

![](https://pic1.zhimg.com/80/v2-14fe1e23adbea49df366b25444981f6c_720w.webp)

当然也可以ctrl + p，输入excalidraw命令新建绘图

![](https://pic1.zhimg.com/80/v2-a6453f3c8e6fd35f5550d304d4f6a0f4_720w.webp)

鼠标右键创建的绘图会保存于当前文件夹下，而点击左侧图标或是通过命令创建的绘图会保存于根目录下(默

认)，也可以通过excalidraw插件的设置进行自定义

![](https://pic4.zhimg.com/80/v2-d36fd86e454c61588d13248b7e51fa1f_720w.webp)

## 2. excalidraw命名

在 excalidraw设置-文件名 中可进行**自动生成名称**更改

![](https://pic1.zhimg.com/80/v2-2fd8f0ee7761029031b428c2916cf574_720w.webp)

包括**前缀，中间部分，和日期时间，扩展名**等

![](https://pic4.zhimg.com/80/v2-06d4ce6be00c79c5109b613d30bfdb3b_720w.webp)

### 2.1 **兼容性设置**

建议关闭旧格式相关选项，以旧格式创建的excalidraw

绘图因为是.excalidraw文件，而非.md文件，无法在库内搜索到

![](https://pic2.zhimg.com/80/v2-58a74d26ee7a087bc18fcb1298cd40e9_720w.webp)

### 2.2 模板设置 Template

文件夹中创建Template模板文件，设置中保存模板文件位置，注意Template文件后缀，新格式与扩展名都会影响，如果是新格式，且后缀名为.md，直接用名字即可，设置模板文件后，新建绘图其实就是复制模板文件

![](https://pic3.zhimg.com/80/v2-27da557a87c47d01dc31a84a6ea613b2_720w.webp)

![](https://pic3.zhimg.com/80/v2-841e23f17946cb164221b828c5678356_720w.webp)

## 3. **画板移动与缩放**

使用**ctrl + 鼠标滚轮**/**鼠标滚轮**进行缩放，左下角会显示缩放比例，点击可自动恢复到100%

![](https://pic1.zhimg.com/80/v2-c50f5fc8c979e81279085ed5fb4ae13c_720w.webp)

其效果可在第三方插件配置的 **显示** 中进行更改

![](https://pic4.zhimg.com/80/v2-d33a028c79f37345ca2c87d17327758b_720w.webp)

按住 **空格 + 鼠标左键**，可在当前缩放等级下进行**自由拖动**

其效果等于选择上方功能条的hand tool

![](https://pic1.zhimg.com/80/v2-910337b1fa6fe8f13d69a0b5ffc54514_720w.webp)

## 4. 选择和删除

**鼠标左键单击**进行选择，无背景图形需要点击边框进行选择

![](https://pic4.zhimg.com/80/v2-6f13ba67e67e462c2790c2021c2f1def_720w.webp)

**shift + 鼠标左键点击**，进行多选

![](https://pic1.zhimg.com/80/v2-5f6c40e86340f6d2c699e92067b70464_720w.webp)

或者**按住鼠标左键**，拖动进行框选

![](https://pic4.zhimg.com/80/v2-1fd211a24ea2ea3fc8dc90de3bb57f7b_720w.webp)

选择后点击**delete键/backspace退格键**，可删除所选

## 5. 图形绘制

使用鼠标选取或数字键选取，按住鼠标左键拖动绘制图形，包括 **四边形、菱形、圆形、箭头、线段**五类

![](https://pic1.zhimg.com/80/v2-45a0b94b4c99d100149e6b99cb1a019c_720w.webp)

其中，箭头和线段 以通过鼠标左键连续点击，改变线条形状，按 **esc** 键结束绘制，可自行按鼠标左键多次点击形成的点位调节其形状

![](https://pic1.zhimg.com/80/v2-24ef800009e4229b00fa13ae19025360_720w.webp)

**注意**，绘制箭头时，箭头与图形之间有附着区，在此区域内开始/结束箭头绘制，可以使箭头跟随图形移动，线段则无此功能(同时箭头形态可以通过**Arrowheads** 自定义)

![](https://pic1.zhimg.com/80/v2-54486baf8cb17611846b06ce94bdf160_720w.webp)

![](https://pic2.zhimg.com/80/v2-d88b3046b9f552a0583e1a3e7c568e15_720w.webp)

## 6. 图形样式调整

在按住鼠标左键拖动框选，或者点击有线条部分选中图形后，左侧会自动呼出样式调整界面(默认情况)

![](https://pic2.zhimg.com/80/v2-70d834e7527b57f4573f57d89743fa99_720w.webp)

### 6.1 stroke

改变图形边线或线段的颜色，点击右侧颜色区域可进行进一步精细调整，选取不同颜色(其固定色板颜色调整将在后文说明)

![](https://pic1.zhimg.com/80/v2-43b2bb5c846f64ea449efe122e4d74d8_720w.webp)

你也可以使用十六进制颜色编码，或者取色器进行颜色修改

---

![](https://pic1.zhimg.com/80/v2-852aa5e47ca520935e01d22d1f95551c_720w.webp)

### 6.2 Background

图形内部颜色填充，其颜色修改与上文中stroke的颜色修改机制类似

![](https://pic2.zhimg.com/80/v2-db77e5f12e933d88d03cc62e084bdb8d_720w.webp)

### 6.3 Fill

图形内部填充样式（当背景色不为透明时）就是三种：斜线填充，交错线填充，完全填充

### 6.4 Stroke width

图形或线段宽度，**注意**：填充Fill里面的斜线和交错线条宽度同样受此影响

### 6.5 **Stroke style**

实现与虚线切换

### 6.6 **Sloppiness**

图形与线条的凌乱度，主要模仿手涂的质感

### 6.7 Edge

影响图形或线条边角尖锐 还是 圆滑

![](https://pic3.zhimg.com/80/v2-88ba4f07618e4d62b3c92ec9a07494c6_720w.webp)

### 6.8 Arrowheads

选择箭头后，可自定义箭头起始段和终端的箭头形态

![](https://pic1.zhimg.com/80/v2-999b99acc6e43170d748bb69b77ecdd0_720w.webp)

### 6.9 **Opacity**

选择图形或线段的不透明度

### 6.10 **风格复制**

框选图形，右键菜单 copy style/Paste style

（快捷键的风格粘贴貌似不行）

![](https://pic2.zhimg.com/80/v2-b65c1feccce0fdfdada3aaf963eee4a9_720w.webp)

### 6.11 **线条/箭头编辑技巧**

选择线条、箭头，**右键菜单-Edit line**，或者使用快捷键 **ctrl + enter**，进行细节调整，可自动切分多段(注意 edge是直线，还是弧线)

![](https://pic3.zhimg.com/80/v2-0b69b95bd591977146b82967e7304b82_720w.webp)

绘制线条、箭头时候，按住**shift**可以限制线段在固定角度运动，有助于**画平行/垂直线等**(比如给图形或导入

PDF标注时)

## 7. 图形空间位置调整

### 7.1 图形移动与旋转

**图形移动**：框选后，鼠标左键按住拖动即可

**图形旋转**：款选后，将鼠标移动到上方小点处，光标变为手形后，按住鼠标左键即可进行旋转操作

![](https://pic2.zhimg.com/80/v2-b8716d6032c8b37b2276685e486bd56d_720w.webp)

### 7.2 Layers图层

![](https://pic1.zhimg.com/80/v2-d82d0032e1ae211de46c7bf45164d660_720w.webp)

从左至右

**send to back**：将图形降到最后一层

![](https://pic1.zhimg.com/80/v2-d25ac64d7c62b71fc3daa38726ab0ce8_720w.webp)

**send backward**：图形下降一层（非首层图形）

![](https://pic2.zhimg.com/80/v2-190fae029d4d665cc0e2c36cad3e35e9_720w.webp)

**Bring to front**：图形升到最上层

![](https://pic4.zhimg.com/80/v2-109dc96ab44f8aed2a40bf023ebacb13_720w.webp)

**Bring forward** ：图形上升一层

![](https://pic1.zhimg.com/80/v2-4783b349cc79a131a8f48ad4196ac028_720w.webp)

### 7.3 Align排列

框选多个图形后，可对其相对位置和距离进行调整左、列、右对齐 + 平均左右间距上、行、下对齐 + 平均上下间距

![](https://pic4.zhimg.com/80/v2-516611fc0ae7b51f9cd98ebfbb44e6f3_720w.webp)

### 7.4 **group selection图形组合**

框选多个图形后，可组合或分解图形(**注意**：此处的

group跟后面图形嵌入markdown的group是一个意思) 快捷键：**Ctrl + G**

![](https://pic3.zhimg.com/80/v2-c937c483cc423ca00b3cc4ca737b5b62_720w.webp)

### 7.5 **图形左右/上下翻转**

选择一个或多个图形

右键菜单-Flip horizontal（左右翻转）右键菜单-Flip horizontal（上下翻转）

![](https://pic1.zhimg.com/80/v2-06f3d1636ae1d60603e34424771b4d24_720w.webp)

### 7.6 **图形复制与删除**

excalidraw图形复制有几种方式，我最为常用的是 **alt + 鼠标左键**可以单个复制，也可以框选复制多个

![](https://pic2.zhimg.com/80/v2-d85dffdb7a1015a59c7cdb393e3bb325_720w.webp)

其他还有常见的**ctrl + c/v**，右键菜单复制粘贴以及使用呼出面板的**Duplicate**

![](https://pic2.zhimg.com/80/v2-a84572830630b7671ba86c072ed9fd51_720w.webp)

删除：框选后**按delete键**，或者点击Actions中的删除按钮

## 8.**画板设置**

进入excalidraw后，鼠标左键点击空白区域，左上角可见呼出面板标识(默认情况)

![](https://pic2.zhimg.com/80/v2-93f9b8048a8a72e99f9b482c03b5d285_720w.webp)

### 8.1 **背景颜色及风格调整**

通过**Canvas background**及**Dark mode**可以调节**画板背景颜色**以及画面亮暗风格

同时在插件设置-显示一栏中，可以设置画板亮暗即

Dark mode与obsidian风格匹配

其中 Dynamic styling一项是指更改颜色等的呼出面板的色彩是否随背景颜色调整而调整(match color)，也可选灰色调但随之调整(grey color)，当然也可以不随之更改(OFF)

![](https://pic3.zhimg.com/80/v2-7cc66d07db74457efcaec306791bf002_720w.webp)

### 8.2 托盘模式 Toggle tray-mode

页面风格调整，呼出面板位置由左上该为左下或右下，同时，右上部分库和笔配置由横向改为纵向同时框选图形后默认不呼出调整面板(可点击绘画按钮切换是否呼出)，改为手动调整，托盘位置可通过设置调整

![](https://pic3.zhimg.com/80/v2-40b4112f8f893ad8a675680e2bddc196_720w.webp)

![](https://pic4.zhimg.com/80/v2-c02cd5aafe8b99e9d63eb486bcb95c9b_720w.webp)

### 8.3 保存

可通过呼出面板save保存，或者 ctrl + s

![](https://pic3.zhimg.com/80/v2-e9d7e2f18261ca7f20972ec875ab8f3e_720w.webp)

或者点击右上角保存按钮

![](https://pic1.zhimg.com/80/v2-cba09cf4f7133da1af98571084b44630_720w.webp)

或者 在 **设置-保存**中，设置自动保存时间

![](https://pic2.zhimg.com/80/v2-d3e41c5244ab6aa675e5efb46ea0532d_720w.webp)

### 8.4 方格 show grid

空白处右键菜单，选择show grid，开启背景方格

![](https://pic4.zhimg.com/80/v2-9670eaf7a0fbe92567afddd284c936cf_720w.webp)

此时，图像的移动会以小方格为基本单位(按ctrl键拖动则正常移动)，而关闭方格背景则移动单元更小，更丝滑

![](https://pic4.zhimg.com/80/v2-e88243214e834bc6b22d55ec9c42181b_720w.webp)

绘制线条的时候，线条也会跟随方格，同时CTRL键则自由移动，便于绘制

![](https://pic4.zhimg.com/80/v2-93c5ade43d0b55a0614ede74f15529e3_720w.webp)

### 8.5 zen mode/View mode

两种简洁模式，右键菜单点击/快捷键开启

![](https://pic4.zhimg.com/80/v2-685ddd6635cac6f25c1d76d61f6baeaf_720w.webp)

**zen mode**：禅模式，只留下上方图形栏，左右两边配置栏隐藏，选择图形后不再呼出颜色等配置菜单，但仍可以创建和改变单个图形大小等

**View mode**：所有配置栏全部隐藏，只能将所有图形作为整体移动，不可改变图形

### 8.6 图形统计信息 Stats for nerds

右键菜单点击/快捷键开启

![](https://pic2.zhimg.com/80/v2-783fe58983e2679bbfe27ca625b4730d_720w.webp)

显示图中所有元素个数，以及整体长宽占比(作为组考

虑)

选择单个图形，或单个组也可看到x、y坐标、单独长宽及旋转角度等信息

![](https://pic1.zhimg.com/80/v2-1cdbbb9dfe5d01a7f08f62388f576804_720w.webp)

### 8.7 markdown模式 与 绘图模式转换

**转换为markdown**：左上角呼出面板-open as markdown

![](https://pic1.zhimg.com/80/v2-aab15efd6aee70698e2a40a99014727c_720w.webp)

或者，右上角点击3点按钮-打开为markdown文件

![](https://pic3.zhimg.com/80/v2-c0a5ea69c8eca964c24c62335d5ffeb6_720w.webp)

**转化为excalidraw绘图**：右上角3点按钮-打开为excalidraw绘图

![](https://pic1.zhimg.com/80/v2-05c7a10f146c07fdc691716d55a0c8d0_720w.webp)

## 9. 文件嵌入Excalidraw

obsidian文件嵌入快捷键图示

![](https://pic4.zhimg.com/80/v2-68ae70ee835f3eeb824f66f00a198647_720w.webp)

### 9.1 **通用库内文件嵌入insert命令**

ctrl + p打开命令面板-输入insert any file

![](https://pic2.zhimg.com/80/v2-b3affa50874434328a50d2931be37ca9_720w.webp)

或者点击页面右上角 insert any file按钮

![](https://pic1.zhimg.com/80/v2-17cd9f06775448a70427031a16441e68_720w.webp)

几乎所有库内文件可以按照iframe框架或image形式嵌入

![](https://pic1.zhimg.com/80/v2-d64480b96f142f5ae85dc3e4601ce60c_720w.webp)

iframe的主题色(light,dark)是否跟随主题色变化，可以在设置中调整

![](https://pic2.zhimg.com/80/v2-f36db4ad1889201af609830e087425f9_720w.webp)

### 9.2 markdown文件嵌入

1. 拖入+快捷键
2. **!****[[****文章名****#标题****]]****{换行字符数}** 嵌入文本内容
3. ctrl+p 打开命令面板，输入insert any le
4. tool panel中点击insert markdown按钮

### 9.2.1 拖入 + 快捷键：

直接拖入会变成文字+链接拖入后按住鼠标左键，会提示按快捷键组合

![](https://pic1.zhimg.com/80/v2-fa7e5247cde6915a4420c9bed06f9168_720w.webp)

此时，按 **ctrl/shift**即提示 image形式嵌入，大小可自行调整，嵌入image显示内容多少可通过excalidraw设置调整

![](https://pic1.zhimg.com/80/v2-cd7cade0caec09e94cbd0aeecb072484_720w.webp)

其中嵌入宽度与高度设置数值会影响图像中文本显示内容，太小会显示不全，其本质上就是从上到下显示当然，也可以转换为markdown文件后，自行调整

**[[** **文章名** **#标题** **|宽度x最大高度** **]]**

![](https://pic2.zhimg.com/80/v2-b235c620b13c6ca6ce3627f45a3e4025_720w.webp)

**鼠标左键拖入 + ctrl + alt**，提示以100%图像形式嵌入 excalidraw，图形可移动，不可改变大小，可转换成

markdown形式后更改，删去100%，即等于 ctrl/shift导入image

![](https://pic1.zhimg.com/80/v2-0dd8d0ac78e36d2e2de9d021396b4e0c_720w.webp)

**鼠标左键拖入 + ctrl + shift**，以iframe互动框架形式嵌入，可保留obsidian md文件格式，自由调整大小双击后可直接进行编辑，且其左上角可进行整个文档/ 标题段落/具体文段的展示切换

![](https://pic3.zhimg.com/80/v2-bb3bdcf91c2af68fab9c5ce79a403b36_720w.webp)

### 9.2.2 以文本形式嵌入

双击绘图空白处输入文本

**![[文章名#标题]]{换行字符数}**

![](https://pic3.zhimg.com/80/v2-1ff59b213d1ccefaf89183f6e8c8686a_720w.webp)

以文本形式嵌入，没有markdown格式，不能在绘图内调整，只能跳转到原md文件内调整，最重要没有 markdown的文档搜索功能，只能手打输入

其默认折行字数(40)可以在设置内更改，也可自己在{?} 中定义

![](https://pic4.zhimg.com/80/v2-f8ec66e21814b012df9bba715a27397b_720w.webp)

### 9.2.3 insert file按钮

可以以image形式插入，跟按拖入按ctrl的形式一样

![](https://pic1.zhimg.com/80/v2-90571eb147c8559c8344144d01e25584_720w.webp)

### 9.3 **PDF文件嵌入**

ctrl + p 打开命令面板-insert PDF file/tool panel-insert pdf按钮/拖入页面按ctrl

![](https://pic3.zhimg.com/80/v2-9311908bb60ec57714050a294cd7f01a_720w.webp)

**page to import**：导入页数可按逗号区分，可导入多页，作者建议20页左右，导入太多会比较吃内存，而且每次加载都要重新从PDF渲染，当然这还是得看电脑，可以自行测试一下，油管Zsolt自己做了个测试， i9+64G内存，导入347页PDF，打开逐页渲染要个几十秒，后面使用还是比较丝滑的

后面一次是添加边框(border box)、导入后页面锁定（不可调整）、列数（没啥用，默认即可）、页面间距

**imported page size**：不会影响分辨率，放大后查看同样清晰，但是会影响插入页面和字体大小

此外，通过命令面板insert any le去插入/拖入页面 + ctrl + shift,来导入iframe形式的pdf ，不过体验一般，页数过多很吃资源嵌入的pdf可以**改变大小，背景颜色，边框颜色**等， **ctrl + 鼠标左键可以打开PDF文件**，并跳转到当前页面

![](https://pic1.zhimg.com/80/v2-1cc2c947d17ba33ab9b706ee5af90030_720w.webp)

![](https://pic3.zhimg.com/80/v2-ea92d91d3d73d1bcdb49a2abf56cebaa_720w.webp)

### 9.4 **SVG文件嵌入**

tool panel - 点击insert svg按钮

![](https://pic2.zhimg.com/80/v2-cdda8c9835c2f39e84f56b119608c519_720w.webp)

选择库内svg文件嵌入，这样嵌入的svg文件可进行编辑

![](https://pic3.zhimg.com/80/v2-3fd751e3a0761b7efcda5f0a88d996e6_720w.webp)

而库内/库外拖入的svg则只是图片形式

### 9.5 网页内容嵌入

所有网页内容复制网址可直接嵌入网页

油管、推特等按住网页拖入 + ctrl +shift，嵌入对应可调整大小视频，体验更好诸如，豆瓣，amazon电子书平台，拖入书籍图片或复制图片链接，可嵌入在线网页图片，而不导入库中

![](https://pic4.zhimg.com/80/v2-472d3aa06e3b96ea6f4c4dfd222b98d7_720w.webp)

### 9.6 **LaTex公式嵌入**

tool panel-点击insert LaTex按钮

![](https://pic1.zhimg.com/80/v2-5581f5ba6c58857e178faa62b1f91928_720w.webp)

![](https://pic1.zhimg.com/80/v2-0c0c34d0537cc4cc41afbd3b96994aa4_720w.webp)

输入公式后回车即可在页面中看到

**ctrl + 鼠标左键** 点击可进行更改

![](https://pic4.zhimg.com/80/v2-5be68254beabe7547a1d8b4e18b05d1f_720w.webp)

### 9.7 **数据表格导入**

文本中的数字，或excel中的简单数字可以复制，在绘图中粘贴时，自动形成简单表格(对应关系不能太复杂)

![](https://pic4.zhimg.com/80/v2-d2ce98324a44992613beefb530b2e203_720w.webp)

![](https://pic2.zhimg.com/80/v2-d274215dcdb9441b314f5721736e9779_720w.webp)

![](https://pic1.zhimg.com/80/v2-6f1250d19dd471b8449c1592f03ee8f4_720w.webp)

## 10. 链接与Excalidraw绘图文件嵌入

### 10.1 **链接**

选择excalidraw任意图形，点击左侧链接按钮/ctrl+k/ 右键菜单-creat link，都可以创建对库内文件的链接，以链接形式输入文件名即可，可直接修改和删除 ctrl + 左键点击该图形：在新窗口打开链接文件

ctrl + shift + 左键点击该图形：在当前窗口打开链接文件

ctrl + alt + 左键点击该图形：在分窗口在右侧打开链接文件

![](https://pic1.zhimg.com/80/v2-9d433626ae71d70a37a471427020be04_720w.webp)

### 10.2 内部链接 link

选择excalidraw任意图形，点击 tool panel-内部链接按钮，点击link，即可生成指向该图形的内部链接

![](https://pic3.zhimg.com/80/v2-699c56f6fa50cdcfc8402d76f26ea79e_720w.webp)

![](https://pic2.zhimg.com/80/v2-d76c08aa35c9f9c7c998d73aa7431b89_720w.webp)

此时，链接已经成到剪贴板，可复制到excalidraw形成页内跳转(ctrl + shift + 左键点击)，可编辑|别名来缩短显示

![](https://pic3.zhimg.com/80/v2-11eb179ceba5a343e19f8cf863c69de2_720w.webp)

### 10.3 **内部链接 area/group**

同样选择图形，点击 tool panel-内部链接按钮，点击 area/group同样可以生成area/group的嵌入式链接，可直接复制入markdown文档

除了`**![[绘图名#^area/group=elementid]]` 这种形式外

还可以识别`**# <section name>**`这种形式，即在图形内部输入标识，或者选择多个图形生成group，内部输入标识，如下图(注意该图形**不需要生成area/group链接**，但是group需要将该图形**置入group**中)

![](https://pic1.zhimg.com/80/v2-fa81f74b3fcab0e31b3a6644d8985958_720w.webp)

`**![[绘图名#area/group=方形]]**` 同样可以被识别而且这个绘图名可以是同一个，如下面的例子我将下面文字、黄色图形、人、大黑框四个元素置入同一个组(记得要**保存以更新状态**)

![](https://pic1.zhimg.com/80/v2-fccb347ba532eee0f5f86846666044c0_720w.webp)

我在markdown文件里输入

`**![[** **testDemo#今日计划]]**`将显示文字信息，而且里面计划内容可以直接在markdown 中进行勾选

![](https://pic3.zhimg.com/80/v2-48ba8563bac64540dad7fd44c510450e_720w.webp)

`**![[testDemo#area=今日计划]]**`

![](https://pic3.zhimg.com/80/v2-e0125be6467fa4dfc80568a9fa395cc2_720w.webp)

`**![[testDemo#group=今日计划]]**`

![](https://pic3.zhimg.com/80/v2-36dc44df35bfe9d15da892cfcb798f8e_720w.webp)

### 10.4 Excalidraw绘图文件嵌入

除了上面的area和group嵌入，你也可以整个绘图文件嵌入显示，同时可以更改图像大小和位置

![](https://pic4.zhimg.com/80/v2-4ae6f3d2a638f388099c6ffbccb5c773_720w.webp)

如果嵌入视频和网页等(gif图嵌入绘图不动，但在嵌入 markdown的绘图中会动)，需要更改设置-native svg 才可以显示，不然只能显示网址的占位符

![](https://pic4.zhimg.com/80/v2-eff8d02cc9bec5a8c7fda02c4c316457_720w.webp)

此外，作者视频中提到的一种用法也可以拿来借鉴，他将一张大型油画图片导入excalidraw中，然后框选其中各个部分，输入`**# <section name>**`，然后将此部分透明化，从而可以在markdown 中对各部分进行说明与学习，可以用于诸如地图，医学绘图等的学习中(注意右键菜单-锁定位置lock以避免操作而导致图像移动)

![](https://pic2.zhimg.com/80/v2-cc826230e81b2efb0a1a4ef9bc41091d_720w.webp)

## 11. **导出 export**

选择左侧呼出面板-export image/命令面板-export image

![](https://pic1.zhimg.com/80/v2-27cca825316c1d214dcfcbb487de2a0c_720w.webp)

前两项决定图像大小质量，padding太小，svg导出容易显示不全，后面依次是：亮暗模式输出、是否带背景颜色、一次性设置/保留设置、是否嵌入excalidraw场景、保存位置是库中绘图位置/选择电脑文件位置然后点击输出文件形式

![](https://pic4.zhimg.com/80/v2-f03a69d59c3308640f03d28ba0e9fd2b_720w.webp)

当然如果只需要几个图形的输出，可以选择多个图形，然后右键菜单-png/svg输出

![](https://pic2.zhimg.com/80/v2-9017c344ffb15ad05da4f01805f18b89_720w.webp)

## **12.字体更改与文本**调整

下载合适字体文件，置入obsidian当前库在电脑中的文件夹(我直接丢入Excalidraw文件夹，但都能识别) 打开设置-启用本地字体，选择对应字体  

![](https://pic2.zhimg.com/80/v2-fdc1c0b6c3d0813e3774d9e40cafe7bd_720w.webp)

  
在excalidraw中双击输入文字，左侧呼出面板可调整为中文字体，并且调整文字位置，大小  

![](https://pic3.zhimg.com/80/v2-c2e32d86d1edcebe94aaca7bbe37f7fe_720w.webp)

## 13. 图形嵌入文字(箭头-便利贴)

箭头线段可以双击嵌入文字

![](https://pic1.zhimg.com/80/v2-cd8a4c1c4709da825009be259174b618_720w.webp)

三种封闭图形都可以嵌入文字，形成便利贴效果，同样右侧可以调整文字大小、位置

![](https://pic3.zhimg.com/80/v2-88243361898ed1817db25941e7812142_720w.webp)

**注意**：直接拖动放大/缩小文字大小不变，每行显示内容变多/少，shift + 拖动放大/缩小 文字大小随之改变

![](https://pic2.zhimg.com/80/v2-6362f5e1f9e0f50c303df8744f7b2211_720w.webp)

## 14. 库文件 library

点击右上角library图标，打开库文件

![](https://pic4.zhimg.com/80/v2-530bb0c79578eb3fbbe2b180f214e417_720w.webp)

### 14.1 搜索下载库文件

点击页面下方 **browse library**按钮，打开Excalidraw libraries网页，关键词搜索/根据上面的分类进行检索

![](https://pic2.zhimg.com/80/v2-5e37a39bd4f08a6616feb212c56101c9_720w.webp)

如下载量(Total Downloads)，点击Download下载 (add to Excalidraw是针对网页应用的)

![](https://pic1.zhimg.com/80/v2-69ebb43e253fee306f77fd12a796f4e4_720w.webp)

下载后选取文件夹存放即可

![](https://pic3.zhimg.com/80/v2-174488ae286ebbe0096aa2df6561858e_720w.webp)

### 14.2 使用库文件

点击右上角3点-open-选择下载库文件，拖出来使用即可

![](https://pic4.zhimg.com/80/v2-1661ff28c0ece7de78f6fa3071d1228f_720w.webp)

### 14.3 建立个人库

他人库中文件，绘制图形，导入svg文件等都可以组合成各种图形然后 选择图形-右键菜单-**add to library**

![](https://pic2.zhimg.com/80/v2-ae935058d64de8026cb39c00f22ef05d_720w.webp)

即可添加到个人库

![](https://pic3.zhimg.com/80/v2-51d48edd785e8fdf64c3282621a7cc96_720w.webp)

勾选个人库中文件，点击右上角3点，选择save to，可建立个人库文件

![](https://pic4.zhimg.com/80/v2-47247c2051a142286b0fbac78427e8ff_720w.webp)

![](https://pic2.zhimg.com/80/v2-a1e21171c8af387105e322fd29a3a825_720w.webp)

### 14.4 **删除库文件**

勾选文件，点击右上角3点-删除remove

![](https://pic4.zhimg.com/80/v2-0e2eec8275a231ebdd4da5798a73a4ef_720w.webp)

或者**全部删除**：点击右上角3点-**Reset library**

![](https://pic4.zhimg.com/80/v2-1d446b18e462b23d9666dcb29bd0e59b_720w.webp)

## 15. 笔设置

### 15.1 笔数量设置

excalidraw设置-自定义画笔的数量

![](https://pic2.zhimg.com/80/v2-a93b90b5a021d91a825d88886bf42b49_720w.webp)

![](https://pic1.zhimg.com/80/v2-f3ef389f405a8535f5dfda28619ac4dc_720w.webp)

### 15.2 **笔性质设置**

双击任意笔，可打开pen setting

![](https://pic3.zhimg.com/80/v2-e7af817a964288a8342229fac7fe8086_720w.webp)

笔画设置项很多，不一一说明，简述几个重要设置

**Pen Type**：插件中设置7种默认笔类型，切换笔类型，点击Apply应用则可更换当前笔类型，也可做为返回默认设置而使用

**Stroke & ll applies to**：是说使用笔设置后，其他图形绘画时候，颜色是否要跟随笔设置，开启则为不跟随

**Preset color**：则是反过来，用笔时候相应颜色是否要跟随绘图时候的颜色变化

## 16. 脚本 Script

### 16.1 脚本安装和更新

点击左侧呼出面板script library/右上角脚本库按钮，进入脚本安装面板

![](https://pic1.zhimg.com/80/v2-1195dfd26be6c1cfbac059007719f7a8_720w.webp)

![](https://pic2.zhimg.com/80/v2-f09d6f1dbdee158d8e628c27f386c715_720w.webp)

可搜索安装

![](https://pic3.zhimg.com/80/v2-260cc14985dbdc9ed25dafa2b8c81c32_720w.webp)

更新同样在库中，需要更新的脚本右侧有相应文字提醒

![](https://pic1.zhimg.com/80/v2-b2cc0fc5f060cb1ba85eda23dda78778_720w.webp)

### 16.2 脚本管理

可在脚本下载文件夹下新建相应主题文件夹，alt多选脚本文件置入创建文件夹下

![](https://pic1.zhimg.com/80/v2-08058251614860678ccc0aa004360278_720w.webp)

同样在tool panel中也会进行相应归类

![](https://pic4.zhimg.com/80/v2-0445b4078effb1cd001253f338343933_720w.webp)

### 16.3 脚本快捷使用

打开工具面板，在脚本列表里选择一个脚本，**鼠标左键长按**，则会在笔工具后面添加一个此脚本的快捷方式，便于常用脚本使用，再次长按取消

![](https://pic3.zhimg.com/80/v2-de3a01c48ec06a8585c6718ad51c8e86_720w.webp)

![](https://pic3.zhimg.com/80/v2-377bda78b75dfe4732fb88363332899e_720w.webp)

托盘模式，能纵向显示

## 17. 重要脚本功能讲解

### 17.1 幻灯片slideshow

![](https://pic3.zhimg.com/80/v2-755bd9aa52ff8475d1ff362494bbf06e_720w.webp)

补充，幻灯片插件1.9.21版本后可使用激光笔工具

![](https://pic2.zhimg.com/80/v2-a7c4e87f683f0a4e56d1141b6305e245_720w.webp)

### 17.1.1 slideshow-箭头模式

使用箭头工具，汇出需要显示的多端界面，然后点击

slideshow按钮(要选择箭头路径才有效)，进行幻灯片播放

进入播放模式可看见控制框(可移动)

![](https://pic3.zhimg.com/80/v2-0cc2eccc04e745455a67a1400f1ffbb2_720w.webp)

![](https://pic2.zhimg.com/80/v2-4403c329c220bd7701eef04c2c9ed5ed_720w.webp)

控制左右的好理解，主要讲一下切换箭头显示开关和编辑按钮

开关打开后，箭头线段后台隐藏，便于进行图像调整，而且默认是选中的，所以可以直接点击slideshow运行幻灯片播放

而点击旁边编辑按钮后，箭头线段可见，编辑模式就是选择箭头后 右键菜单-edit line/ctrl + enter，可移动创建多个节点，节点 退格/del 可删除

![](https://pic4.zhimg.com/80/v2-032c3e18830898b0e871e618b6f8d2d3_720w.webp)

### 17.1.2 # Frame tool 模式

点击工具栏/按F键，四边形框选内容

![](https://pic1.zhimg.com/80/v2-d22b5f94a8911b6348290c4d31db47d4_720w.webp)

有点类似与group功能，框选内容

![](https://pic3.zhimg.com/80/v2-29625888aee9b6b75e99d5d2f02ed426_720w.webp)

此时点击slideshow可进行幻灯片播放，注意frame上方数字就是播放顺序，你可以更改数字内容以更改播放次序，同时也可以往框架内填入内容(双击直接更改，更改时有点模糊)

![](https://pic3.zhimg.com/80/v2-24b60ab895472d8b3d1c4aaa255fff72_720w.webp)

点击框架(边框)右键菜单可选择所有元素-内容框选

移除所有元素-不是删除，类似于解除group，内容脱离框架

![](https://pic3.zhimg.com/80/v2-f3013277f63cf61382f4f528d90d2522_720w.webp)

### 17.2 默认颜色更改 palette loader

![](https://pic3.zhimg.com/80/v2-953ddaa37b0947374bc4f259caa1fc82_720w.webp)

安装完脚本点击脚本按钮

![](https://pic4.zhimg.com/80/v2-1b7676622b87818226528a07e04375d3_720w.webp)

显示3种功能

![](https://pic3.zhimg.com/80/v2-f286dade39c21e84b9454acd2e721f46_720w.webp)

**Load palette from file**

实际上就是用于恢复默认颜色的，在设置中有介绍设置文件夹放入之类的，可识别但没啥用

![](https://pic4.zhimg.com/80/v2-6769879ebcaa50e04c3c734cd19fa7c3_720w.webp)

**Set top~**

可用于设置呼出面板的五种基本颜色

首先在excalidraw中设置五个黑边填充色块，如下图

![](https://pic2.zhimg.com/80/v2-19cc04d23c964052aeffe80bd09a1995_720w.webp)

框选后，点击脚本-Set top~

然后可选择更改背景、填充、线条颜色更改

![](https://pic4.zhimg.com/80/v2-fd0512aade719408c940f54e952b3eeb_720w.webp)

![](https://pic3.zhimg.com/80/v2-12c03a88bc4319e9635f97843f92edd2_720w.webp)

**Copy palette~**

用于复制其他绘图文件的颜色，使用第二个功能改完，可以保存为固定的颜色绘图文件，用于以后颜色更改

![](https://pic4.zhimg.com/80/v2-772248ae7986ad76de9d12806e694243_720w.webp)

### 17.3 位置与大小调整 Set Dimensions

![](https://pic2.zhimg.com/80/v2-5d017d754f9b3166c5cd0ed6589a6d19_720w.webp)

框选图形后，点击脚本按钮

![](https://pic4.zhimg.com/80/v2-6d0a40d76ff87893a87fcd124c03a75f_720w.webp)

![](https://pic3.zhimg.com/80/v2-2f4e12e1a98ad2ead4f56d0f6329cc72_720w.webp)

可以精确更改坐标数据和长宽数据

![](https://pic2.zhimg.com/80/v2-4891f95be6461fadc6d69db4de8c56a9_720w.webp)

### 17.4 更改线条宽度 Set Stroke Width

![](https://pic2.zhimg.com/80/v2-7b30a1b002652ead0a249d767ea51965_720w.webp)

框选图形后，点击脚本按钮，可设置脚本宽度

![](https://pic1.zhimg.com/80/v2-1d8d21ed6ca6712c49f4aeae3d3cd8cc_720w.webp)

默认的宽度数值是1，2，3，4，可作为更改数值的参考

![](https://pic1.zhimg.com/80/v2-52a82963b8af6af7de1a8e2847ac807c_720w.webp)

### 17.5 图形组合 Boolean Operations

![](https://pic3.zhimg.com/80/v2-dab57312239ab76225fc874322719882_720w.webp)

选择两个图形，点击图标，出现如上图中五种选择

![](https://pic3.zhimg.com/80/v2-b2ef0e4a25aadba6873cdf92328a7836_720w.webp)

![](https://pic4.zhimg.com/80/v2-0e5a21d310faf48026558deaf16d4153_720w.webp)

值得注意的是，图层在下的图形被视为a，颜色变化同a

![](https://pic4.zhimg.com/80/v2-801bc7955b1781bde620aa143916a163_720w.webp)

图形与线条同样可行

![](https://pic2.zhimg.com/80/v2-a34982b0143cd812664e6118da54a951_720w.webp)

### 17.6 椭圆分割 split Ellipse

![](https://pic1.zhimg.com/80/v2-5885eb8f54b0080d16b3539a43188bd4_720w.webp)

此脚本作用就是用线条切割椭圆，注意切割对象只能是椭圆，而切割工具也只能是线条，虽然脚本显示可以用椭圆切割椭圆，但目前测试下来bug很多，用线条切割能做出很多效果

![](https://pic2.zhimg.com/80/v2-32bf09d463472e2bb1983cbc44d5b46d_720w.webp)

注意线条贯通就会切割出封闭图形，想切分线段，线条不要贯通椭圆

![](https://pic2.zhimg.com/80/v2-52d8909e8f8febaa59ac4a5265a19391_720w.webp)

### 17.7 图形样式更改

![](https://pic1.zhimg.com/80/v2-1bf969c739ee6741bb89a9d826b6b4fc_720w.webp)

选择图形，点击change shape(也可通过命令输入)

![](https://pic2.zhimg.com/80/v2-965ad974c4209dc87028eb67eb50a131_720w.webp)

可进行基本图形更改(不更改可 **esc键** 跳过)

![](https://pic2.zhimg.com/80/v2-b640a06874f2700cf649c8c09abf5ba1_720w.webp)

然后选择填充样式(不更改同样可esc键跳过)

![](https://pic1.zhimg.com/80/v2-4ef79da91c696f4a2923efdbf3207e74_720w.webp)

## 18. **补充**

### 18.1 视觉词汇积累

大家绘画能力大都没有那么好，所以除了导入svg， png这种方式外，作者还提到一种类似隔纸临摹的技巧，就是从网上截图一张图片，然后把透明度降低，用线段临摹，然后保存到库里，或是用文本标识

![](https://pic4.zhimg.com/80/v2-e442978aa4399f816b954be0dac25a13_720w.webp)

注意，切换线条的时候，透明度要换回来

## 1.9.20 更新

### 1. 图表工具 Mermaid to Excalidraw

点击**more tools - Mermaid to Excalidraw**

![](https://pic4.zhimg.com/80/v2-9388a80e248fc26c3977dceca8df923f_720w.webp)

使用**mermaid语法**创建各种图表(流程图，甘特图等)

![](https://pic4.zhimg.com/80/v2-2f4e9ad1b303a97ae98ef4fefd9a084b_720w.webp)

点击图中 **flowcharts** 链接，进入语法教学网站，并且网站上有实时预览和示例内容可供参考(点击右上角Live Editor)

![](https://pic2.zhimg.com/80/v2-f206c7ac0fee05a55e0b2600a0fcacfd_720w.webp)

插入的部分图表(如：甘特图)，alt + 左键点击可再次编辑

![](https://pic2.zhimg.com/80/v2-0a440d08e30104517efc79f934cd2375_720w.webp)

### 2. 对齐指导线

移动图形时按住ctrl键，会出现对齐指导线

![](https://pic2.zhimg.com/80/v2-ebc2f5b1d1025ab8052131fce177aaa1_720w.webp)

## 1.9.21激光笔 laser pointer

more tools - laser pointer，或快捷键 K

![](https://pic2.zhimg.com/80/v2-ce80a5897fc9635a3f40348e1fcfcbbd_720w.webp)

作用模拟老师讲课时，用激光笔提示重点的效果，可以画出一段1-2秒内消失的红线

点击其他绘图工具取消选择

在幻灯片模式中，点击下方按钮，同样可以使用此功能

![](https://pic2.zhimg.com/80/v2-a7c4e87f683f0a4e56d1141b6305e245_720w.webp)

### 1.9.28 激光笔设置

更新后， 在excalidraw插件设置-**显示**-**Laser pointer**中可以对**激光笔颜色**、**显示时间**、**显示长度**进行设置

![](https://pic3.zhimg.com/80/v2-1b2d5e1da4f5c333a324edf56d01f086_720w.webp)

## 1.9.24 更新

### 1. 将命令转化为链接

语法为 **[[cmd://cmd-id]]**，或者**[描述](cmd://cmd-id)**，cmd-id是可替换内容，是英文的快捷键内容，但有语法改写，需要研究一下

也可以使用命令，ctrl+p打开**命令面板**，输入 **Insert Obsidian Command as a link**

点击需要使用的命令嵌入，点击链接可使用命令

![](https://pic4.zhimg.com/80/v2-89a6767b57f45a6e5ed1ec92708a4e17_720w.webp)

### 2. 嵌入系统图片

更新后，任意文件夹图片，**拖入+ctrl+shift**，将作为图片链接存在，而不会将图片存入obsidian

![](https://pic4.zhimg.com/80/v2-a7739d2ee49a89f18f4ff67e17f08a4f_720w.webp)

## 2.0.0 更新

### 1.从excalidraw创建md文件

以便签(sticky note)形式创建图形文字，**右键菜单-convert to file**，即可创建markdown文件，位置是当前excalidraw所属的文件夹

![](https://pic4.zhimg.com/80/v2-ea41beaa47bedc223d28d3737cfc1d43_720w.webp)

填入markdown名称

![](https://pic1.zhimg.com/80/v2-c38a98b9762e83b3a1c684ac53df9118_720w.webp)

转换为嵌入的markdown文件

![](https://pic2.zhimg.com/80/v2-df10d8d94344cba8930d75c06e0343f5_720w.webp)

## 2.0.1 更新

### 1. 同比缩放嵌入文档

使用 **shift + 拖动缩放** 来进行视频、嵌入markdown和PDF等嵌入文档的调整不会破坏原有比例及可读性

![](https://pic3.zhimg.com/80/v2-75d2162f882faff966668d66f41c4d1a_720w.webp)

### 2. 嵌入文件设置菜单

双击嵌入markdown文档，点击左上角设置按钮，对嵌入文档样式进行设置

![](https://pic2.zhimg.com/80/v2-8c604a7a676003c16719075e77756f75_720w.webp)

在**取消主题匹配**的前提下(**Use Obsidian Defaults**)，可对嵌入文档样式进行更改

**Filename Visible：**文档名显示(如上方游鲦亭记)

**Background color：**背景颜色调整。匹配自定义元素背景/匹配excalidraw画板背景，透明度调整

**Border color：**边框颜色调整。同上

**注意**：透明度需要适度调低，不然无法显示背景条纹变化

![](https://pic4.zhimg.com/80/v2-2c9774a340a3990a3e899dcfc2517327_720w.webp)

## 2.05 更新

### 1. 本地文件拖入

现在支持本地视频(目前仅MP4)，音频(MP3)，gif等文件嵌入excalidraw

默认按住 **ctrl + shift + 拖入** 实现

### 2. 链接&拖入快捷键配置

在**excaidraw设置-显示-Link Click and Drag&Drop~**中，可以对各项链接&拖入文件实现的快捷键组合进行更改

鼠标悬停显示键位名称，我只更改了一个点击链接在新页面打开

![](https://pic1.zhimg.com/80/v2-b47639410395870a873b06de2036fb7c_720w.webp)

## 2.0.15-2.0.19 更新

### 1. 图片切剪与蒙版

选中图片，ctrl + p 打开命令面板，输入裁剪（英文版直接输入 crop即可），选择裁剪与蒙版

![](https://pic4.zhimg.com/80/v2-5f7093033ca8bdab12352d05edfff00b_720w.webp)

此时将在右侧打开另一个编辑框

![](https://pic3.zhimg.com/80/v2-281d5b51d415d7e1f51918deac63328a_720w.webp)

可以进行基本的裁切操作，完成后鼠标点击excalidraw页面等待刷新

![](https://pic3.zhimg.com/80/v2-d21bb13fa6ff88bda5041d3f0999ced6_720w.webp)

此外，你可以在蒙版页面添加图形遮罩和字体遮罩以达到部分透明的效果(图形遮罩必须纯黑，字体则所有颜色都是透明效果)

![](https://pic1.zhimg.com/80/v2-7bc9412d631ed426b5e3b31a08cb33d4_720w.webp)

将黑色图形遮罩铺满，再添加一个白色图形遮罩，可以部分露出图片(其他颜色有轻微色调变化)

![](https://pic4.zhimg.com/80/v2-30bd64c2e10bcc8aa7493697e61188ab_720w.webp)

在这个基础上，你可以选取一些色彩艳丽的图片，黑色图形遮罩后，添加上白色文字，就形成了有设计感的彩色字体

![](https://pic1.zhimg.com/80/v2-02c61398071e2efd4474a15849784db8_720w.webp)

在 **看板** 中依然可以ctrl+p使用蒙版命令对图片进行修改

![](https://pic1.zhimg.com/80/v2-02c61398071e2efd4474a15849784db8_720w.webp)

### 2. pdf 剪切与蒙版

在excalidraw中打开pdf，在需要裁切的页面 ctrl+p，键入裁切与蒙版，打开蒙版页面中是对应pdf当前页的内容

![](https://pic1.zhimg.com/80/v2-aec7b487637702eee159d4b3091a84f8_720w.webp)

裁切需要的图形，会以excalidraw绘图文件形式出现在当前pdf右侧

![](https://pic1.zhimg.com/80/v2-862a499260a2bc8800a0efc8731faef8_720w.webp)

ctrl+左键点击，可以选择跳转到蒙版页面继续编辑，或者跳转到pdf的当前页

![](https://pic3.zhimg.com/80/v2-e4194d257c6f18adadad461cc8adca26_720w.webp)

你也可以在md文件中嵌入pdf页面链接,链接选取后ctrl+p-剪切与蒙版来使用

![](https://pic4.zhimg.com/80/v2-516bd8076e856bb9d117590a514f456f_720w.webp)

在pdf阅读器中直接选择文字信息右键复制到选取的链接，链接选取后ctrl+p-剪切与蒙版来使用

![](https://pic2.zhimg.com/80/v2-93c9830eedd77a605646f7d620444771_720w.webp)

![](https://pic2.zhimg.com/80/v2-3746278e79fd5bf680ce1b7969596c71_720w.webp)