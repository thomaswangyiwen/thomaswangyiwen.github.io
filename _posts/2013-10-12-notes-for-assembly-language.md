---
layout: post
title: "notes for assembly language"
description: ""
category: "Low-level"
tags: [Assembly]
---
{% include JB/setup %}

这是一篇汇编为主的学习笔记，同时，我尽量把它写成一个面向编程经验不多的同学的tutorial。但是你必须熟悉一些计算机硬件软件的基础知识，毕竟这是关于较low-level programming的日志。笔者使用的环境:

+ Ubuntu 12.04 LTS
+ GCC toolset

##Linux环境简述

Linux的历史，是什么等等知识，在这里我就不赘述了，很多书还有网路资料都有很详细的讲解。另外，不出意外的话，以下更多内容我也只会把相应需要的材料进行说明，其它留给读者自己去查阅。重申一遍，我在这里只说明学习Assembly language所需要的必要知识。

我们虽然常常说"linux"有众多发行版本，但是"linux"指的是众多版本中共有的部分--kernel。kernel是linux操作系统的核心部件，它可以监控一切操作系统中发生的事。kernel的存在把人们从硬件相关的交互操作、文件操作、进程间交互等琐碎的事中解脱出来，大大降低了我们的工作量。

##三种语言

在这系列网络日志中，我们将涉及三种语言的概念：

[Machine language](http://en.wikipedia.org/wiki/Machine_language "Machine language")

[Assembly language](http://en.wikipedia.org/wiki/Assembly_language "assembly language")

High-level language(http://en.wikipedia.org/wiki/High-level_programming_language "high-level")

这些概念详情可以参考以上名词的wikipedia，我已经把它们超链接好了，点开看一看就好。

##硬件环境简介

在这我们简单地大概介绍一下硬件基础知识。

我们现在pc中使用的硬件架构几乎全是Von Neumann architecture（现在ARM架构的平板如果也算pc的话，那就另说了）。数据和运行的程序呢，都会在RAM中得以临时存储。

为了操作RAM中的数据和程序，我们当然还得有CPU。cpu会从ram中每次读取一段指令，然后执行。这叫一次fetch-execute cycle。

最简单的CPU应包含以下单元：

+ Program Counter: 在每次fetch-execute cycle开始时，program counter保存了等待执行的instruction的内存地址，用来告诉CPU从哪儿读取instruction并执行。每个cycle开始，cpu都要检测Program Counter。

+ Intruction Decorder：CPU读取完了instruction，这些内容就会传递到这里翻译成具体的执行指令的操作，例如加减乘除啦、分配新的内存空间啦。

+ Data Bus：这是链接CPU和RAM的一排线。它的作用是负责CPU和RAM的通信，所有CPU-RAM中间互动操作要经过BUS。

+ General-purpose registers：registers是cpu内部的高速存储单元（相对于和RAM交互而言，cpu-ram相对来说慢得多）。一般而言它们分为General-purpose registers和special purpose registers。

+ Arithmetic and logic unit：cpu所需处理data和decoded instructions都会送到这里。这是intructions真正执行的地方。

## some important terms

+ pointers: 被内存存储起来的地址。值得一提的是，CPU之所以可以知道intructions在内存中的地址是因为我们有一类special-purpose registers--instruction pointers帮助我们确定指令在内存中的位置。