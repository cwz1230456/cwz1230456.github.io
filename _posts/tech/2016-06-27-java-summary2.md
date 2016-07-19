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


