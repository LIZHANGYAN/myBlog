---
title: C++基础
date: 2017-12-18 15:58:18
tags:
  - C++
  - 语言
categories:
  - 就会这么点语言
---
{% asset_img c1.png C++ %}
<!-- more -->

# C++简介
**C++**是一种静态类型的、编译式的、通用的、大小写敏感的、不规则的编程语言，支持过程化编程、面向对象编程和泛型编程。

## 面向对象四大特性

<li> <strong>封装</strong>
<li> <strong>抽象</strong>
<li> <strong>继承</strong>
<li> <strong>多态</strong>

## 三大部分

<li> <strong>核心语言</strong>，提供了所有构件块，包括变量、数据类型和常量。
<li> <strong>C++标准库</strong>，提供了大量的函数，用于操作文件、字符串等。
<li> <strong>标准模板库 STL</strong>，提供了大量的方法，用于操作数据结构。

## C++环境设置
C++编译器和文本编辑器/IDE。

### GUN 编译器
GNU 的C/C++编译器是最常用的免费编译器。
<li> <strong>UNIX/Linux上的安装</strong>

  > <a href="http://gcc.gnu.org/install/">GCC安装教程</a>

<li> <strong>Mac OS X 上的安装

  > 安装Xcode <a href="http://developer.apple.com/technologies/tools/">Xcode下载</a>

<li> <strong>使用Visual Studio</strong>

  > <a href="https://www.visualstudio.com/">VS 2015下载</a>

# C++数据结构

## 基本的内置类型

<li> bool
<li> char
<li> int
<li> float
<li> double
<li> void
<li> wchar_t 宽字符型

  > 可以用**signed,unsigned,short,long**修饰

**如图所示**:
{% asset_img datatype.png C++ %}

## typedef 声明

使用typedef为已有的类型取一个新名字。
`typedef int feet;`

## 枚举类型
若干常量的集合
形式：
```
enum 枚举名{
    标识符[=整形常数],
    标识符[=整形常数],
    ...
    标识符[=整形常数]
} 枚举变量;
```
  > 默认情况下，第一个名称的值为**0**，以此类推，也可以给名称赋予一个特殊的值，只需要添加一个初始值即可。

  例如：
  `enum color{red, green=5, blue}`
  > 这里blue默认值为6，但red仍为1。
