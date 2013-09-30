---
layout: page
title: Wayne's Laboratory 
tagline: Simple and Elegant
---

## Welcome to my page


## Update Author Attributes


    
    title : My Blog =)
    
    author :
      name : Thomas Wayne
      email : vero-org@live.cn
      github : github.com/thomaswangyiwen
      twitter : N\A


    
## Sample Posts



Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## To-Do



