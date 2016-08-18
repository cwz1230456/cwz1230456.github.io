---
layout: post
title: CSS学习（一）
category: 技术
tags: CSS
keywords: CSS，总结，学习
description: 
---

# CSS学习（一）

> CSS╮(╯▽╰)╭

## ID和CLASS选择器

    #para1{text-align:center;color:red;} 
    .center{text-align:center;}
    
## 对某标签内进行操作

    body{background-color:#b0c4de;}
    body {background-image:url('paper.gif');
        background-repeat:repeat-x;//水平平铺
        background-position:right top;//背景图片位置}

简写：

    body {background:#ffffff url('img_tree.png') no-repeat right top;}
    当使用简写属性时，属性值的顺序为：
    background-color background-image background-repeat background-attachment background-position
