---
aliases: 
category: 知识
state: 不紧急且不重要
tags:
  - MATLAB
  - 数据处理
from:
  - zhidao
url:
  - https://zhidao.baidu.com/question/395514645800495045.html
stars: 
created: "2024-05-20 12:07"
updated: "2024-05-28 12:28"
dg-publish: 
---

```matlab
xlb=get(gca,'XTickLabel');%得到原本x轴的标注，是一列字符串、不含百分号、
n=length(xlb);%得到标注的个数，即长度  
a='%';  
per=repmat(a,n,1);%构造一个相同长度的%的列  
new_xlb=[xlb,per];%把百分号加到原标注的后面，即两个列字符串拼起来  
set(gca,'XTickLabel',new_xlb); %将新的标注设为当前x轴的标注
```