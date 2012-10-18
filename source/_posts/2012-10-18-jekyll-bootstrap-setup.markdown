---
layout: post
title: "jekyll bootstrap 配置"
date: 2012-10-18 22:03
comments: true
categories: [jekyll, jekyll bootstrap]
---

## 1.修改配置


执行命令: nano _config.yml

将permalink: /:categories/:year/:month/:day/:title/修改为permalink: /:categories/:title/。

将title修改为你的Blog名称,production_url修改为你的github域名.

去disqus注册帐号并新建站点,将设置的英文名放到 comments->disqus下的short_name.

如果使用google分析,将你在google分析新加的站点的跟踪码放到analytics->google的tracking_id部分.




## 2.编辑首页


执行命令: nano index.md

修改title部分为你的首页名称,将不需要的部分删除,只需 保留原来的

        <ul>
        \{\% for post in site.posts \%\}
        <li><span>\{\{ post.date | date_to_string \}\}</span> &raquo; <a href="\{\{ BASE_PATH \}\}\{\{ post.url \}\}">\{\{ post.title \}\}</a></li>
        \{\% endfor \%\}
        </ul>


