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
<%
var colorToLabelMap = {
    "#f9e196": "重点",
	"#f0bbcb": "方法",
	"#b9e8b9": "结果",
	"#5fb236": "结论",
	"#2ea8e5": "大纲",
	"#f994b6": "GAP",
	"#00ffff": "问题",
    "default": "暂时未分类 " 
};
var labelToShow = colorToLabelMap[it.color] || colorToLabelMap["default"];
%>

[!note] <span style=" background:<%= it.color %>"><%= labelToShow %></span>
<font color="#000000"><%= it.imgEmbed %><%= it.text %></font>
<% if (it.comment) { %>
---
<%= it.comment %>
<% } %>