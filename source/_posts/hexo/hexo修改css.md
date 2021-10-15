---
title: 网站修改
categories: hexo
tags:  [hexo, css]
index_img: http://cpblog.cn/api/img/api.php
date: 2021-1-12 23:10:21

---



### 修改code颜色

在主题跟目录设置里,加入自己的css样式

![image-20211013002635316](https://cdn.jsdelivr.net/gh/q3190872366/img/20211013002635.png)

![image-20211013002702936](https://cdn.jsdelivr.net/gh/q3190872366/img/20211013002702.png)

[data-user-color-scheme='dark'] 
  .markdown-body 
    :not(pre) 
      & > code 
        background-color rgba(94,114,228,1) !important
        transition background-color 0.2s ease-in-out !important

css转换网站  https://www.w3cschool.cn/tools/index?name=sass_tools

色卡  https://tool.solstice23.top/color/