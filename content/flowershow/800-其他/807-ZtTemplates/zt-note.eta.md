---
aliases: 
category: 
state: 
tags: 
from: 
url: 
stars: 
created: "2024-05-02 15:27"
updated: "2024-05-28 12:28"
dg-publish: 
---
## 基础信息

| 属性           | 信息                                 |
| ------------ | ---------------------------------- |
| **标题翻译**     | "<%= it.shortTitle %>"             |
| **作者**       | "<%= it.creators %>"               |
| **出版年份**     | "<%= it.date %>"                   |
| **期刊**       | "<%= it.publicationTitle %>"       |
| **期刊等级**     | "<%= it.libraryCatalog %>"         |
| **标签**       | "<%= it.tags %>"                   |
| **附件链接**     | "<%= it.fileLink %>"               |
| **zotero跳转** | [点这里跳回zotero哈](<%= it.backlink %>) |

> [!note]- 论文摘要
> <%= it.abstractNote[[0]].replace(/\n/g, '') %>
> 

## 论文注释

<%~ include("annots", it.annotations) %>