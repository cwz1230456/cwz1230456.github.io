---
layout: post
title: java学习（三）
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# java学习（三）

> 学习java，重点与c与c++作对比，总结不同点

## 多态

多态是同一个行为具有多个不同表现形式或形态的能力，多态性是对象多种表现形式的体现。

    现实中，比如我们按下 F1 键这个动作：
    如果当前在 Flash 界面下弹出的就是 AS 3 的帮助文档；
    如果当前在 Word 下弹出的就是 Word 帮助；
    在 Windows 下弹出的就是 Windows 帮助和支持。
    同一个事件发生在不同的对象上会产生不同的结果。

多态存在的三个必要条件:①继承②重写③父类引用指向子类对象
