---
layout: post
title: java学习（五）
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# java学习（五）

> 学习java，重点与c与c++作对比，总结不同点

## 重写
返回值和形参都不能改变。即外壳不变，核心重写！

    class Animal{
       public void move(){
          System.out.println("动物可以移动");
       }
    }
    class Dog extends Animal{
       public void move(){
          System.out.println("狗可以跑和走");
       }
    }
    public class TestDog{
       public static void main(String args[]){
          Animal a = new Animal(); // Animal 对象
          Animal b = new Dog(); // Dog 对象
          a.move();// 执行 Animal 类的方法
          b.move();//执行 Dog 类的方法
       }
    }

## 重载
方法名一致，但参数不同，即可以说一个方法到另一个方法的重载。

    public class MainClass {
       public static void printArray(Integer[] inputArray) {
          for (Integer element : inputArray){
             System.out.printf("%s ", element);
             System.out.println();
          }
       }
       public static void printArray(Double[] inputArray) {
          for (Double element : inputArray){
             System.out.printf("%s ", element);
             System.out.println();
          }
       }
       public static void printArray(Character[] inputArray) {
          for (Character element : inputArray){
             System.out.printf("%s ", element);
             System.out.println();
          }
       }
       public static void main(String args[]) {
          Integer[] integerArray = { 1, 2, 3, 4, 5, 6 };
          Double[] doubleArray = { 1.1, 2.2, 3.3, 4.4,
          5.5, 6.6, 7.7 };
          Character[] characterArray = { 'H', 'E', 'L', 'L', 'O' };
          System.out.println("输出整型数组:");
          printArray(integerArray);
          System.out.println("\n输出双精度型数组:");
          printArray(doubleArray);
          System.out.println("\n输出字符型数组:");
          printArray(characterArray);
       }
    }
