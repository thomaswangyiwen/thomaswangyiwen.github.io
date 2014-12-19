---
layout: post
title: "Using Jekyll bootstrap to build blog (1)"
description: ""
category: ""
tags: [Jekyll]
---
{% include JB/setup %}

#Some Tips for using Jekyll

Generally speaking, I followed most of Jekyll-Bootstrap's tutorial. But there are some modifications needed to adopt while installing the Jekyll-based blog.
Before we start, I have to say that:

+ I just want to mainly write a summary or memo for my late review. So this is not a pure toturial.

Oh, and here I want to reclaim my computer environment. I'm using Ubuntu 12.04 LTS (debian-based) as my default desktop environment.

Okay, let's do this.

###Setting the environment for Jekyll

Briefly, we need :
+ ruby
+ bundler(if necessary)
+ rubyGem
+ a well-set repository named USERNAME.github.io
+ Jekyll

Before you kick a first time test, you need to pay attention to how Jekyll world really works in a brief. The Jekyll is not a blog software, it is just a generator that helps you to translate your markdown-based posts into HTML format webpages. So it doesn't work automatically and immediately if you modify some files in your local repository. what it means is a following model that you need keep in your mind, always:

	Original Stuffs ----> Intermediate Stuffs <----> Server

The server will present the Intermediate Stuffs generated from the original stuffs, which are in your local repository.  

As for the local testing, please do remember that the latest Jekyll (version 1.2.1) I use is no longer support the following command:

    sudo jekyll --serve

Instead, the jekyll has officially changed the commander to this:

    sudo jekyll serve

###Creating the new pages and posts

   (I will finish this in the following days)
create a new post:

    rake post title="new post"

create a new page:

    rake page name="about.md"
I do believe these commands are quite self-explanatory.
   

###updates your repository

anyway, here I will use a few words to tell you how to update your repository to the latest version without conservation of your history version.

Every time you modify something in your local repository, you may want to apply this change to your remote repository on the github. Run this:

    git add -u .

    git commit -m "ANYMSG YOU LIKE"

    git push origin master

However, more often, you will need to update everything to your remote repository with your latest modification and history record. Run the following code:

    git add .

    git commit -m "ANYMSG YOU LIKE"

    git push origin master

(Actually, I need to spend more time working on Git. Git is relatively new for me)

###Theme modification

Jekyll-bootstrap has officially presented some themes already, if you like. Follow the tutorial in the official site to install your favorite one. However, I'm considering change it upside down by using Bootstrap version 3.0. 