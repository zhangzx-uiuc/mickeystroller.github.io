---
layout: post
title: 使用Github Pages + Jekyll 搭建个人Blog
---

简单介绍了Jekyll配置过程中的关键点和注意事项，包含一些上传github的git操作, 以及一些过程中涉及到的参考资料

Jekyll 配置
---

这里主要介绍 Mac OS 环境的安装，如果是Windows的话需要先安装ruby和ruby gem.

参考[官方教程](http://jekyllrb.com/docs/installation/)
核心其实就是一句

{% highlight ruby %}
$ gem install jekyll
{% endhighlight %}

问题就是，由于GFW的存在... 所以直接这样会卡死不动，而是需要我们改gem源


{% highlight ruby %}
$ sudo gem sources --remove http://rubygems.org/
$ sudo gem sources -a http://ruby.taobao.org/
{% endhighlight %}

修改完源之后在使用gem安装jekyll，如果报错，就改为：

{% highlight ruby %}
$ sudo gem install jekyll
{% endhighlight %}

如果再报错“Failed to build gem native extension”，很可能是没有安装rvm，可以敲入下面的命令：

{% highlight ruby %}
$ curl -L https://get.rvm.io | bash -s stable --ruby
{% endhighlight %}

到此jekyll就安装完成了,下面安装一个Markdown解释器:

{% highlight ruby %}
$ sudo gem install jekyll rdiscount
{% endhighlight %}

然后在_config.yml里面设定 markdown: rdiscount

到此jekyll配置完成，cd到根目录下,输入下面命令即可运行。

{% highlight ruby %}
$ jekyll server --watch 
{% endhighlight %}

<br>

基本Git操作
---


1. git status (查看当前状态)
2. git add . (stage全部文件)
3. git commit -m "commit message" (commit)
4. git branch (查看所有branch以及目前所在的branch)
5. git branch master (切换到master branch)
6. git push origin master (提交到服务器)


<br>

Reference
---

1. [Github Pages 官方文档](pages.github.com)
2. [Git 官方文档](http://git-scm.com/about)
3. [Markdown 语法说明](http://wowubuntu.com/markdown/basic.html)
4. [Jekyll 官方文档](http://jekyllrb.com/docs/installation/)
5. **[使用Github Pages建立博客](http://beiyuu.com/github-pages/)**



