---
layout: post
title: "fedora 18 安装ruby 开发环境"
date: 2013-04-06 05:42
comments: true
categories: ruby 
---

首先安装rvm

    $ curl -L https://get.rvm.io | bash -s stable

开启autolibs，自动安装依赖

    $ rvm autolibs enabled

安装ruby 

    $　rvm install 1.9.3


设置ruby版本

    $ rvm use ruby-1.9.3-p392  --default
    $ ruby -v  
    ruby 1.9.3p392 (2013-02-22 revision 39386) [x86_64-linux]



使用sdutlinux ruby 源

    $ gem source -r http://rubygems.org/    
    $ gem sources -a http://ruby.sdutlinux.org/

安装rails 

    $ gem install rails --no-rdoc --no-ri
    $ rails -v 
    Rails 3.2.13

