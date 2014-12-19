---
layout: post
title: "using jekyll to build a blog(2)"
description: "This article maily talks about building a blog by using Jekyll and post them on github"
category: ""
tags: [Jekyll]
---
{% include JB/setup %}
###Installation ruby for Ubuntu
check out the Ruby official site for ruby installation:
On an Ubuntu 14.04.1 LTS version(on my computer), since we are using a debian based system, all we need is to run a line of code in the terminal:

	sudo apt-get install ruby-full

Indicated by the official site https://www.ruby-lang.org/en/documentation/installation/###apt ,the system will automatically install Ruby 1.9.3. However, in my case, the apt only fetched the 1.9.1 from the mirrors.


###Install latest rubygems

rubyGems is a part of debian-based system so we don't have to install it from the very beginning. However, Ubuntu has officially limited arbitrary update in case that we may do harm to threaten the stability of the system. For instance, instructed by the rubyGem site, if we run this :

	gem update --system

we will get a runtime error message:
	
	ERROR: While executing gem ... (RuntimeError) gem update --system is disabled on Debian, because it will overwrite the content of the rubygems Debian package, and might break your Debian system in subtle ways. The Debian-supported way to update rubygems is through apt-get, using Debian official repositories. If you really know what you are doing, you can still update rubygems by setting the REALLY_GEM_UPDATE_SYSTEM environment variable, but please remember that this is completely unsupported by Debian.

The solution would be using an older version two-step upgrade commands:

	sudo gem install rubygems-update
	update rubygems

if you want to update to a specific version, you can have some alternative in the first row, for example, in case of rubygems 2.4.5:

	sudo gem instlal rubygems-update -v 2.4.5

After getting the previous steps done, go check the version number of rubyGems:

	gem -v

It will show the latest version number hopefully.

###Install jekyll using RubyGems

Using the following code to install jekyll:

	gem install jekyll

I encountered one problem on my computer. It said that "RDoc is not a full Ruby parser and will fail when fed invalid ruby programs". It also indicated:

	(NoMethodError) undefined method `name' for ###<RDoc::RubyToken::TkLPAREN:0x00000003c6ef28>

This is a typical rdoc problem. we can solve it by renewing the rdoc:
	
	gem install rdoc

###Installing a JavaScript runtime
The last step of the installation would be setting up a JavaScript runtime. I decided to use node.js. First, download the lastest tar package from the node.js official site and retract all files in that package.

###Running Jekyll!
change the current directory to the website root directory and run the following command:

	jekyll serve

###Writing posts
first we should have rake installed:

	sudo apt-get install rake