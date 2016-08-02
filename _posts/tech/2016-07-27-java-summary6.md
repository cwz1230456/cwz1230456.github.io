---
layout: post
title: java学习（六）————多线程
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# 多线程

> 学习java，重点与c与c++作对比，总结不同点

## 为什么使用多线程

首先要明确程序是并发执行而不是串行执行的，例如：程序中有两个子系统需要并发执行，这时候就需要利用多线程编程

## 创建

Java提供了两种创建线程方法：

①通过实现Runable接口

②通过继承Thread类本身

## Runable接口

    //创建一个新的线程
    //implements后面跟的是接口，表示实现接口(可以是多个）；
    class NewThread implements Runnable {
     Thread t;
     NewThread() {
        // 创建第二个新线程
        t = new Thread(this, "Demo Thread");
        System.out.println("Child thread: " + t);
        t.start(); // 开始线程
     }
     // 第二个线程入口
     public void run() {
        try {
           for(int i = 5; i > 0; i--) {
              System.out.println("Child Thread: " + i);
              // 暂停线程
              Thread.sleep(50);
           }
       } catch (InterruptedException e) {
           System.out.println("Child interrupted.");
       }
       System.out.println("Exiting child thread.");
     }
     }
    public class ThreadDemo {
     public static void main(String args[]) {
        new NewThread(); // 创建一个新线程
        try {
           for(int i = 5; i > 0; i--) {
             System.out.println("Main Thread: " + i);
             Thread.sleep(100);
           }
        } catch (InterruptedException e) {
           System.out.println("Main thread interrupted.");
        }
        System.out.println("Main thread exiting.");
     }
     }
