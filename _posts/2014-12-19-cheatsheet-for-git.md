---
layout: post
title: "Cheatsheet for git"
description: ""
category: ""
tags: [Git]
---
{% include JB/setup %}

###Version control tool: Git
Git is a version control tool. Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

Git is different from other VCS(Version Control system, eg: Subversion) because Git records detailed changes in the file while the other systems just keep copies of the whole files.

###Installation of Git
On a debian-based system, we have an elegant way of installing things. We may use apt tools to install git:

	sudo apt-get install git

###First time setup
Now that Git is on your system. In order to use it, you need to customize Git environment.

####Setting up your identity and editor
To set your user name and e-mail address so that Git can commit using them:

	$ git config --global user.name "USERNAME"
	$ git config --global user.email "email@email.com"
	$ git config --global core.editor sublime

Go check your configurations by typing following codes:

	$ git config --list

###repository operations
Initialization of a new project:

	$ git init
	$ git add *.c
	$ git add LICENSE
	$ git commit -m 'initial project version'

Cloning an exisiting repo:

	$ git clone https://github.com/xxx/yourRepo

Checking the status of your files:

	$ git status

Tracking New Files:
	
	$ git add 

Committing your changes:

	$ git commit



