---
title: "版本管理工具 - git使用笔记"
layout: post
date: 2023-12-06 17:18
tag: 
- 随笔
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: false
description: "随笔"
category: blog
author: Fahseki
externalLink: false
---

## 基本介绍

一、使用git进行版本管理

1.1 github已有项目-将代码clone到本地
{% highlight raw %}
git clone https://github.com/Fahseki/Fahseki.github.io.git
{% endhighlight %}
接下来就可以本地修改代码了

1.2 本地已创建项目，想要将项目纳入git管理之中，以下操作会将目录下文件全部纳入版本控制
{% highlight raw %}
git init
{% endhighlight %}
如果后续有新的文件，以下命令将指定文件，提交到git仓库中
{% highlight raw %}
git add 
{% endhighlight %}


二、修改与同步

2.1  本地修改后，查看当前发生修改，显示有变更的文件
{% highlight raw %}
git status
{% endhighlight %}

2.2 将修改提交到本地仓库
{% highlight raw %}
git commit
{% endhighlight %}

2.3 将本地仓库同步至远端分支，进行合并
{% highlight raw %}
git push
{% endhighlight %}

三、冲突解决

3.1 回退版本
{% highlight raw %}
git reset HEAD^            # 回退所有内容到上一个版本  
git reset HEAD^ hello.php  # 回退 hello.php 文件的版本到上一个版本  
git  reset  052e           # 回退到指定版本
{% endhighlight %}


四、协同编辑

4.1 创建分支
{% highlight raw %}
git checkout [branch_name]
{% endhighlight %}

4.2 切换分支
{% highlight raw %}
git switch [branch_name]
{% endhighlight %}

4.3 拉取远端分支代码，进行合并
{% highlight raw %}
git pull
{% endhighlight %}
