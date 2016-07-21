---
layout: post
title: java学习（二）
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# java学习（二）

> 学习java，重点与c与c++作对比，总结不同点

## 继承
继承中最常使用的两个关键字是extends和implements。

①extends

    // A.java
    public class A {
        private int i;
        protected int j;
     
        public void func() {
     
        }
    }
    
    // B.java
    public class B extends A {
    }


类A其实是Object的子类，这里B类是继承A类的，B实例拥有A所有的成员变量，但是对于private的i，B类无访问权限

②implements

Implements关键字使用在类继承接口的情况下， 这种情况不能使用关键字extends。

        public interface Animal {}
        
        public class Mammal implements Animal{
        }
        
        public class Dog extends Mammal{
        }

## 多态

多态是同一个行为具有多个不同表现形式或形态的能力，多态性是对象多种表现形式的体现。

    现实中，比如我们按下 F1 键这个动作：
    如果当前在 Flash 界面下弹出的就是 AS 3 的帮助文档；
    如果当前在 Word 下弹出的就是 Word 帮助；
    在 Windows 下弹出的就是 Windows 帮助和支持。
    同一个事件发生在不同的对象上会产生不同的结果。

多态存在的三个必要条件:①继承②重写③父类引用指向子类对象
