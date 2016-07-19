---
layout: post
title: java的特点及总结
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# java的特点及总结

> 开始学习java，重点与c与c++作对比，总结不同点

## 宏观上看java特点（07-19）
1.创建类，public class **

2.创建主方法，public static void main（String args[]）

3.foreach语句，遍历数组

4.Java大小写敏感

5.所有的Java 程序由public static void main(String args[])方法开始执行

## 关于引用类型
在Java中，引用类型的变量非常类似于C/C++的指针。

引用类型指向一个对象，指向对象的变量是引用变量。这些变量在声明时被指定为一个特定的类型，比如Employee、Pubby等。变量一旦声明后，类型就不能被改变了。

对象、数组都是引用数据类型。

所有引用类型的默认值都是null。

一个引用变量可以用来引用与任何与之兼容的类型。

例子：Site site = new Site("Runoob")。

## 关于类和对象
package test;

public class test {
	public test(String name){
		System.out.println("His name is " + name);
	}
	
	public static void main(String args[])
	{
		test mytest = new test("Tommy");
	}

}

