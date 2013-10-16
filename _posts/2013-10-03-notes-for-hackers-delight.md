---
layout: post
title: "底层操作笔记（1）"
description: ""
category: "Low-Level"
tags: [C,note,hack]
---
{% include JB/setup %}

##0. Computer Arithmetic & Ordinary Arithmetic
Computer Arithmetic（CA） 和 Ordinary Arithmetic（OA）的区别是，CA是有限整数域上进行计算的。在这里提一下T.Tao写的Analysis里有通过公理化构造自然域的方法。我觉得对于理解CA和OA，使用T.tao通过Peano公理构造自然数域的角度来是非常合适的。因为那样去理解，CA和OA的唯一区别就是：CA运算的数域允许且必须存在某一个数字$$n$$的后继$$(n++)$$是第一个数字$$0$$。而OA，或者说自然数域（Analysis书中构造的是自然数域，整数是类同的），则彻底避免了出现这样的循环。

当然，我们也可以跳过这些细节，直接通过基本数论知识来理解。CA上的四则运算是对均是$$2^{n}$$的模运算，n是计算机自身支持的最大字长(Word size of the machine)。虽然如今计算机普遍支持64位，但32位程序在今日依然是主流，在这，我们暂时默认程序都是32位的。掌握32位后向64位的拓展是不难的。所以以下32位环境下的terms我们可以记一记

####Important Terminology

+ bits	      : 1  bit
+ nibbles     : 4  bits
+ bytes       : 8  bits 
+ halfwords   :	16 bits
+ words	      : 32 bits
+ doubleword  :	64 bits

####Fundamental of C

* C 语言中$$true$$是non zero，$$false$$是zero
* do-while 循环是先执行do，再执行判断expression 

####environment reclamation:

#####instruction set
我们使用使用RISC机器作为默认环境，即three-address、超过16个通用寄存器（默认32位长）。0号寄存器永远为零。

另外，机器使用两套RISC 指令集，basic RISC 和 full RISC，分情况使用。指令集的操作只涉及两个sources和一个target。在这里不做赘述。

#####execution time
* 所有指令执行是一个cycle（乘除、取余除外）。
* load immediate算一个或者两个cycles。
* load和store不计延迟时间
* 允许instruction-level parallelism：independent operations被编写成使用8个寄存器，在5个周期内执行。拥有无限指令级别并行能力

##1. Basics

####Bit manipulation

$$ x\&(x-1)$$

$$ x\&(x+1)$$

$$ x\&(-x )$$

