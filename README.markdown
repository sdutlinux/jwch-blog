# 山东理工大学教育技术中心博客 使用指南

你要安装ruby环境，可以查看这个教程。

	http://li.dashuang.name/rails/2012/05/26/ubuntu-1204-install-rails-development-env/

**注意**

	现在使用rsync 同步,在外网也是可以的!!!

## clone远程库

	$ git clone git@github.com:sdutlinux/jwch-blog.git

## clone 主分支

	$ git checkout -b master origin/master



>通过git
>clone获取的远端git库，只包含了远端git库的当前工作分支。如果想获取其它分支信息，需要使用”git
>branch  –r” 来查看， 如果需要将远程的其它分支代码也获取过来，可以使用命令” git
>checkout -b 本地分支名 远程分支名”，其中，远程分支名为git branch
>–r所列出的分支名， 一般是诸如“origin/分支名”的样子。如果本地分支名已经存在，
>则不需要“-b”参数。

## 设置github

可能你不能部署,到gh-pages 分支，需要执行下面的命令

	rake setup_github_pages

然后，添加git地址为

	git@github.com:sdutlinux/jwch-blog.git

## 安装依赖包

	$ bundle install

## 写博客

	rake new_post["title"]

## page

	rake new_page["page"]

## 生成静态页
	rake generate

## 部署

	rake deploy
	这里只提交gh-pages 分支

## 将本地源码提交到master 分支

	git push origin master

## 现在使用我们自己的服务器，这样部署

	rake rsync


