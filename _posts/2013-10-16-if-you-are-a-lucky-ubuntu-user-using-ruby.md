---
layout: post
title: "如果你是个ruby爱好者恰好又用Ubuntu..."
description: ""
category: ""
tags: []
---
{% include JB/setup %}
这篇日志是关于rails4.0的环境搭建。之所以取这个题目，是因为我碰见了一个很恶搞的消息，折磨了我大概一个小时才弄明白来龙去脉：
    "It looks you are one of the happy ubuntu users,
    RVM packaged by ubuntu is old and broken..."

算了不管那么多了。只是写一篇日志来记录一下解决方案。

##遇到的问题
今天遇到的问题是在为一台新的电脑设置rubygem时碰到的。我是通过编译方式安装ruby2.0后，试图安装gem时却遇到了经典的Zlib无法识别的问题。一旦我调用ruby2.0，就会提示zlib未找到。奇怪的是我已经安装过了zlib1g和zlib1g-dev，重新编译ruby2后仍然无法解决这个问题。于是开始想办法装上这个zlib，以便让ruby重新编译，然后正常运行。

##解决的办法
最佳的解决办法还是通过RVM安装Ruby。自己编译安装ruby经常会产生一些很诡异的问题，并且解决起来要比rvm麻烦得多。首先在这里要说明一下ubuntu这个系统很讨厌的地方：

+ 第一,ubuntu的源更新简直慢得一B。至于在ruby上，最新的包也就是ruby1.9.3-full。
+ 第二,各种软件包会被搞坏。像这里的ruby-rvm就是一个又老又坏的典型。

那我们如何解决呢？首先，删除低版本rvm：

    sudo apt-get --purge remove ruby-rvm
    sudo rm -rf /usr/share/ruby-rvm /etc/rvmrc /etc/profile.d/rvm.sh

再安装rvm。注意要把curl之类的一些必要的dependencies安装好之后，在terminal中执行如下指令安装rvm和ruby2:

    sudo \curl -L https://get.rvm.io | bash -s stable --ruby --autolibs=enable --auto-dotfiles

安装完毕就可以正常使用rvm和ruby2了。
    
