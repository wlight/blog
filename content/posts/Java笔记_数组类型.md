---
title: "Java笔记_数组类型"
subtitle: ""
date: 2021-03-11T08:52:52+08:00
lastmod: 2021-03-11T08:52:52+08:00
draft: false
author: ""
authorLink: ""
description: ""

tags: [java]
categories: [java]

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: ""
featuredImagePreview: ""

toc:
  enable: true
math:
  enable: false
lightgallery: false
license: ""
---

<!--more-->

数组是同一数据类型的集合，定义一个数组类型的变量，使用数组类型`类型[]`，例如，`int[]`。数组变量初始化必须使用`new int[5]`表示创建一个可容纳5个`int`元素的数组，整数数组。

特点

- 数组所有元素初始化为默认值，整型都是`0`，浮点型都是`0.0`，布尔型是`false`
- 数组一旦创建后，大小就不可改变。

使用索引来访问数组中的某个元素，索引从`0`开始

修改数组中的元素，使用赋值语句

获取数组大小`数组变量.length`

**数组是引用类型的，如果索引越界，运行时将报错**

```java
public class Main {
    public static void main(String[] args) {
        // 创建一个数组
        int[] ns = new int[5];
        // 赋值
        ns[0] = 1;
        // 访问
        System.out.println(ns[0]); // 1
        // 定义数组时直接指定初始化的元素，不必写出数组大小，由编译器自动推算
        int[] ns1 = new int[]{1,2,3,4,5,6};
        // 进一步简写
        int[] ns2 = {5,4,3,21,1};
    }
}
```

#### 字符串数组

因为字符串也是引用的，所以更改数组的值时，不是更改了字符串的值，而是在新的内存上重新申请了一个字符串，引用到这个新的数组。