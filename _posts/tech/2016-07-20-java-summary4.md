---
layout: post
title: java学习（四）
category: 技术
tags: java
keywords: java,学习,总结
description: 
---

# java学习（四）

> 学习java，重点与c与c++作对比，总结不同点

## 抽象类

①抽象类不能实例化对象，只有被继承才能使用

②为生命类型的就是构造函数，构造函数使类实例化

    public abstract class Employee//声明一个抽象类employee
    {
       private String name;
       private String address;
       private int number;
       //构造函数
       public Employee(String name, String address, int number)
       {
          System.out.println("Constructing an Employee");
          this.name = name;
          this.address = address;
          this.number = number;
       }
       public double computePay()
       {
         System.out.println("Inside Employee computePay");
         return 0.0;
       }
       public void mailCheck()
       {
          System.out.println("Mailing a check to " + this.name
           + " " + this.address);
       }
       public String toString()
       {
          return name + " " + address + " " + number;
       }
       public String getName()
       {
          return name;
       }
       public String getAddress()
       {
          return address;
       }
       public void setAddress(String newAddress)
       {
          address = newAddress;
       }
       public int getNumber()
       {
         return number;
       }
    }
    /*
     *继承
     */
    //声明一个普通类继承于employee
     public class Salary extends Employee
     {
     private double salary; //Annual salary
     //构造函数
     public Salary(String name, String address, int number, double salary)
     {
         //super用于调用父类的构造函数
         super(name, address, number);
         setSalary(salary);
     }
     public void mailCheck()
     {
         System.out.println("Within mailCheck of Salary class ");
         System.out.println("Mailing check to " + getName() + " with salary " + salary);
     }
     public double getSalary()
     {
         return salary;
     }
     public void setSalary(double newSalary)
     {
         if(newSalary >= 0.0)
         {
            salary = newSalary;
         }
     }
     public double computePay()
     {
        System.out.println("Computing salary pay for " + getName());
        return salary/52;
     }
    }
    /*
     *使用
     */
    //声明一个对以上类进行操作的类
    public class AbstractDemo
    {
     public static void main(String [] args)
     {
        //我们虽然不能实例化employee类，但是我们可以实例化salary类
        Salary s = new Salary("Mohd Mohtashim", "Ambehta, UP", 3, 3600.00);
        Employee e = new Salary("John Adams", "Boston, MA", 2, 2400.00);
        System.out.println("Call mailCheck using Salary reference --");
        s.mailCheck();
        System.out.println("\n Call mailCheck using Employee reference--");
        e.mailCheck();
      }
    }
    
## this与super

this： this关键字是类内部当中对自己的一个引用，可以方便类中方法访问自己的属性

super：调用父类的构造函数
