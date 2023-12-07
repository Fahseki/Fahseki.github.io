---
title: "版本管理工具 - git使用笔记"
layout: post
date: 2023-12-06 17:18
star: false
tag: 
- 随笔
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: false
description: "随笔"
category: blog
author: Fahseki
externalLink: false
---

# 基本介绍

## 一、使用git进行版本管理

1.1 若github已有项目-将代码clone到本地
{% highlight raw %}
git clone https://github.com/Fahseki/Fahseki.github.io.git
{% endhighlight %}
接下来就可以本地修改代码了

1.2 若是本地先已创建项目，想要将项目纳入git管理之中，以下操作会将目录下文件全部纳入版本控制
{% highlight raw %}
git init
{% endhighlight %}
使用后，会发现在本地目录下会出现".git”文件夹（如果设置了隐藏文件不可见就会看不到）

然后在github创建项目，将二者进行关联，这一步一般需要ssh key，暂时嫌麻烦没搞，就用1.1的方式也能成功


## 二、修改与同步
一次完整的添加新文件流程：

2.1  创建出一个新的file "README.md"，此时仍未处于git控制下，查看当前文件状态 = Untracked files
{% highlight raw %}
git status
{% endhighlight %}

将文件纳入控制，当前文件状态 = Changes to be committed，代表已被跟踪，处于暂存状态
{% highlight raw %}
git add README.md
{% endhighlight %}

2.2 将修改提交到本地仓库，此时本地会显示"√"
{% highlight raw %}
git commit -m "提交新文件"
{% endhighlight %}

2.3 将本地仓库同步至远端分支，进行合并，这样就可以在github查看到了
{% highlight raw %}
git push
{% endhighlight %}

## 三、冲突解决

3.1 回退版本
{% highlight raw %}
git reset HEAD^            # 回退所有内容到上一个版本  
git reset HEAD^ hello.php  # 回退 hello.php 文件的版本到上一个版本  
git  reset  052e           # 回退到指定版本
{% endhighlight %}


## 四、协同编辑

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


![Markdowm Image](firstBlog/markdown.jpg)
<figcaption class="caption">测试增加一张图片</figcaption>

