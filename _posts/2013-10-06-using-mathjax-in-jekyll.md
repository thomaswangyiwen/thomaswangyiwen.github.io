---
layout: post
title: "using Mathjax in Jekyll"
description: ""
category: ""
tags: [MathJax,Jekyll]
---
{% include JB/setup %}

I am about to write some posts in serious math, so of course I should lend a hand from [MathJax](http://www.mathjax.org "MathJax"), so that I could write LaTeX stuff. Here is how.

###Change the markdown parser to kramdown
In order to use LaTeX, you need to install "kramdown" parser to take the place of the default one. Please visit the website to see more information about [Kramdown](http://kramdown.gettalong.org/syntax.html "Kramdown")

Installation of kramdown is quite easy. In the terminal, type in:

	gem install kramdown

If you are a debian user, you might need to add "sudo" before the above command in the terminal. 

Then change the default setting. Add a line to the "_config.yml" file in your local file as follows:

	markdown: kramdown

Now, the parser's ready. Bullets are loaded.

###Change the front page setting 
Still remember the model of Jekyll we are talking in my earlier post? Jekyll is supposed to generate pages. So, we are required to change the pages so that they can support MathJax. Fortunately, we don't need to get our hands dirty by modifying them one by one because all pages will inherit them from only one page-namely, default.html.

You can find it in:

	/_includes/themes/CURRENT_THEME/

anyway, add a line to the default.html:

	<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

After that, rebuild the whole website. Give it a shot:

$$a^2 + b^2 = c^2$$

$$a_{1} + ... + a_{n}$$