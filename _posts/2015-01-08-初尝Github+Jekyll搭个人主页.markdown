---
layout: post
title:  "初尝Github+Jekyll搭建个人主页"
date:   2015-01-08 18:02:20
categories: jekyll
---


**使用Github+Jekyll搭建个人主页**


> 用Github+Jekyll个人主页总算搭起来了~先占位，稍后补齐~
 
`要说比较逼人的，就是这Win7 64位的系统，还有那个gem下jekyll的过程，另外这个markdownpad的免费版总感觉哪里怪怪的~~#`

* 注册Github账号
* 创建一个仓库
* 下载Github for Windows的客户端
* 使用Github客户端clone那个仓库到本地
* 安装ruby（记得勾选一个添加系统变量的选项），然后是devkit（ruby dk.rb init，ruby dk.rb review 查看ruby的路径能不能打出来，ruby dk.rb install）
* 安装jekyll~gem sources --remove https://rubygems.org/、
gem sources -a https://ruby.taobao.org、
gem sources -l
gem install jekyll
* jekyll new jekyll_demo
* 把jekyll中的内容copy到那个clone下来的空的仓库中
* 在Github客户端中，添加好commit然后sync到github.com
* 访问yourusername.github.io就能看到Welcome to Jekyll!
