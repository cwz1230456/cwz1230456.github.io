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
		//构造函数 我的理解：用构造函数实例化类，使类以一个具体的形式出现，即，类：鸟，实例化化后：鸽子
		public test(String name){
			System.out.println("His name is " + name);
		}
		//类中的方法 我的理解：就是函数
		public void setAge(int age){
			testage = age;
		}
		//我的理解：main之下开始作出使用
		public static void main(String args[])
		{
			test mytest = new test("Tommy");
			mytest.setAge(16);
			System.out.println("His name is " + mytest.testage);
		}

	}
	或者：
	
	package test;

	public class test {
		int testage;
		public test(String name){
			System.out.println("His name is " + name);
		}
		
		public void setAge(int age){
			testage = age;
		}
		
		public int getAge(){
			System.out.println("His name is " + testage);
			return testage;//习惯？
		}
		
		public static void main(String args[])
		{
			test mytest = new test("Tommy");
			mytest.setAge(16);
			mytest.getAge();
			//mytest.setAge(16);
			//System.out.println("His name is " + mytest.testage);
		}
	
	}
	//实例化时所有的参数在主方法中输入即可，主方法以上都是泛泛的定义，无指定值
