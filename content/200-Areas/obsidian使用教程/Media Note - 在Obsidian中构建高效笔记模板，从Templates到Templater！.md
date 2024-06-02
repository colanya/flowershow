---
aliases:
  - templater视频笔记
category: 视频
state: 已完成
tags:
  - obsidian
  - plugin
  - media_note
from: bilibili
url: https://www.bilibili.com/video/BV1c64y1W7c2
stars: 
created: "2024-05-06 15:30"
updated: "2024-05-28 12:28"
dg-publish: 
media: https://www.bilibili.com/video/BV1c64y1W7c2
---
- [00:01:02](https://www.bilibili.com/video/BV1c64y1W7c2?t=62.585624#t=01:02.59) 官方插件
- [00:08:00](https://www.bilibili.com/video/BV1c64y1W7c2?t=480.381526#t=08:00.38) templater
	- [00:10:26](https://www.bilibili.com/video/BV1c64y1W7c2?t=626.138175#t=10:26.14) 常用语句一览
		- ![[Pasted image 20240506155642.png]]
		- [00:10:34](https://www.bilibili.com/video/BV1c64y1W7c2?t=634.684834#t=10:34.68) `<% tp.file.title %>` 插入该文件的标题
		- [00:11:01](https://www.bilibili.com/video/BV1c64y1W7c2?t=661.667606#t=11:01.67) `<% tp.file.creation_date("YYYY-MM-DD") %>` 文件的创建时间
		- [00:11:36](https://www.bilibili.com/video/BV1c64y1W7c2?t=696.267786#t=11:36.27) <% tp.date %> 添加今天、明天、昨天的日期
		- [00:12:04](https://www.bilibili.com/video/BV1c64y1W7c2?t=724.335326#t=12:04.34) `<% tp.system %>` 
			- prompt可弹出对话框，输入信息；
			- suggester可弹出选择框，供选择![[Pasted image 20240506160224.png]]
				- 前面是选项显示的名称，后面是实际填入的内容
				- true代表若不选择则不创建笔记
				- 'status'是注释，引号内填入给用户的提示
		- [00:17:15](https://www.bilibili.com/video/BV1c64y1W7c2?t=1035.985782#t=17:15.99) `< %tp.file.cursor %>` 指定光标开始位置
	- [00:18:06](https://www.bilibili.com/video/BV1c64y1W7c2?t=1086.934206#t=18:06.93) 插入模板
		- `open insert template model`
	- [00:19:56](https://www.bilibili.com/video/BV1c64y1W7c2?t=1196.439655#t=19:56.44) 指定模板文件夹
- [00:21:33](https://www.bilibili.com/video/BV1c64y1W7c2?t=1293.054849#t=21:33.05) 进阶使用
	- [00:21:37](https://www.bilibili.com/video/BV1c64y1W7c2?t=1297.429304#t=21:37.43) 使用别人写好的模板代码
	- [00:26:30](https://www.bilibili.com/video/BV1c64y1W7c2?t=1590.770938#t=26:30.77) capture使用方式
		- 可以将某个内容迅速添加到某篇笔记的某个标题下
	- [00:30:01](https://www.bilibili.com/video/BV1c64y1W7c2?t=1801.593562#t=30:01.59) 插入callout
