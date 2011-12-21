---
published: false
layout: post
title: "octopress+github安装记录"
date: 2011-12-21 11:19
comments: true
categories: 
---
* 在github上创建两个repository， 一个用于保存发布后的帖子，名字可以叫blog, 另一个存放帖子源文件。

{% codeblock %}
rvm install 1.9.2 //使用ruby1.9.2
git clone git://github.com/imathis/octopress.git octopress
cd octopress	
gem install bundler
bundle install
bundle exec rake install
{% endcodeblock %}

* 如何发布帖子，可以参考[这里](http://octopress.org/docs/blogging/)。zsh注意，正确的新建帖子格式：

{% codeblock %}
rake "new_post[帖子标题]"
{% endcodeblock %}

* 帖子发布完成之后，需要手动把./source push 到存放源代码的repository中去。
