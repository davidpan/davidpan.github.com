---
layout: post
title: "使用Jekyll在GitHub上架设Blog"
date: 2012-10-18 21:58
comments: true
categories: [GitHub, Jekyll, Jekyll Bootstrap, Twitter Bootstrap]
---

GitHub很多朋友都知道，目前是做git托管最大的网站。详细介绍请看:[关于Github][1].

Jekyll是ruby开发的静态页面解析器，可非常简单的用于blog的静态页面生成。


## 1.建立GitHub账号


访问注册页面:[Github免费注册页面][2] 。输入用户名(英文+数字)、电子邮箱地址、设置密码(必须包含一个小写字母、一个数字，长度要7位及以上。)，点 $




## 2.新建仓库


注册后登陆GitHub，访问:[Create a New Repo][3]建立新的仓库。仓库名称必须使用如下格式:你的用户名.github.com ,不要选中:Initialize this reposito$




## 3.安装GitHub客户端


Windows下建议安装[GitHub For Windows][4],其他平台可以直接安装Git客户端。

## 4.将Jekyll部署到GitHub

        git clone https://github.com/plusjade/jekyll-bootstrap.git BLOGIT580.github.com
        cd BLOGIT580.github.com
        git remote set-url origin git@github.com:BLOGIT580/BLOGIT580.github.com.git
        git push origin master

_请将BLOGIT580，替换为你的用户名。_

十分钟后打开浏览器，访问BLOGIT580.github.com，就可以看到架设的Blog了。



## 5.Jekyll本地环境部署


ruby环境的搭建请参考: [Ruby On Rails在Ubuntu 12.04.1 LTS下的安装][5]

执行命令:

      gem install jekyll
        cd BLOGIT580.github.com
        rake post title=”hello world ” #新建文章
        rm –rf _post/core-samples/ #清理示例文章
        jekyll –server

_请将BLOGIT580，替换为你的用户名。_

打开浏览器，访问:http://localhost:4000 查看效果。



## 6.更新本地修改到GitHub


执行命令:

        cd BLOGIT580.github.com
        rake post title=”hello world ” #新建文章
        rm –rf _post/core-samples/ #清理示例文章
        jekyll –server

_请将BLOGIT580，替换为你的用户名。_

打开浏览器，访问:http://localhost:4000 查看效果。



## 6.更新本地修改到GitHub


执行命令:

        cd BLOGIT580.github.com
        git add .
        git commit –m “first commit”
        git push

_请将BLOGIT580，替换为你的用户名。_

执行完成后，本地所有修改将同步到远程服务器上。





### 其他建议阅读文档:

*    [Markdown语法说明(简体版)][6]
*    [Jekyll介绍(英文)][7]
*    [GitHub帮助(英文)][8]

[1]: https://github.com/about
[2]: https://github.com/signup/free
[3]: https://github.com/new
[4]: http://windows.github.com/
[5]: http://blog.it580.com/install-ruby-on-rails-on-ubuntu-12-04-1-lts
[6]: http://wowubuntu.com/markdown/
[7]: http://jekyllbootstrap.com/lessons/jekyll-introduction.html
[8]: https://help.github.com/

