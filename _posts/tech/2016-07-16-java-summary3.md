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

## 关于数组的声明与操作、Arrays类

    import java.util.Arrays;//引入Arrays这个包
    public class array_equal {
    	public static void main(String[] args) {
    		int[] array1 = {1,2,3};
    		//数组声明，初始化时应初始化长度。
    		//数组其实就是一个类
    		int[] array2 = new int[10];
    		
    		for(int i=0; i<10; i++){
    			array2[i] = i + 1;
    		}
    		/*
    		for(int i=0; i<10; i++){
    			System.out.println(array2[i]);			
    		}
    		*/
    		System.out.println("array1和array2相等:" + Arrays.equals(array1,array2));
    	}
    }

## 关于Stream

字符流

    package stream;
    import java.io.*;
    public class read {
    	public static void main(String args[]) throws IOException{
    		char c;
    	    // 使用 System.in 创建 BufferedReader 
    	    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    	    System.out.println("Enter characters, 'q' to quit.");
    	    // 读取字符
    	    do {
    	    	c = (char) br.read();
    	        System.out.println(c);
    	       }while(c != 'q');
    	   }
    }
    
字符串流

    package stream;
    import java.io.*;
    public class read {
    	public static void main(String args[]) throws IOException{
    		//char c;
    	    // 使用 System.in 创建 BufferedReader 
    	    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    	    String str;
    	    System.out.println("Enter a line.");
    	    System.out.println("Enter 'end' to quit.");
    	    // 读取字符
    	    do {
    	    	str = br.readLine();
    	        System.out.println(str);
    	      } while(!str.equals("end"));
    	   }
    }
