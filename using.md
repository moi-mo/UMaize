# 配置项

## ```/_include```下

### ````script.html````

第12行的列表，是鼠标点击特效冒出的文字，请按需替换；如不需要此特效，请在```/_config.yml```中26行将extClickEffect项改为```false```。



## ```/_data```下



### ```links.yml```

本文件记录友链信息，请按需替换或添加（可以无限添加）。

请注意yaml语法格式。



### ```menu.yml```

本文件记录header处的菜单。

请注意，header处第一项是博客url，不需要在此文件中配置。



### ```site.yml```

本文件配置Valine与footer。

关于valine的使用，请参考[Valine官网](https://valine.js.org)；请注意，place holder分为一般页面下与微博客页面下两种。

footer项为数组，这一栏中的字符串将被按顺序解析为html代码插入页脚。



## ```/pages```下

该页面下的文件均由markdown文件与html文件组成，请按需更改。请注意Message页面的layout已内置Valine，不需要在页面下方单独添加Valine代码。



## What's more

### 微博客

本功能依赖于Valine，请先配置Valine再配置本功能。



（以下内容摘自TMaize文档）~~写文档好累~~

### 本地运行

一般提交到 github 过个几十秒就可以看到效果，如果你需要对在本地查看效果需要安装 ruby 环境

```
gem install jekyll
gem install bundler
# 第一次运行需要在项目下执行 bundle install
# 国内依赖下载慢可以使用ruby-china的镜像站进行请求重定向
# bundle config mirror.https://rubygems.org https://gems.ruby-china.com
bundle exec jekyll serve --watch --host=0.0.0.0 --port=8080
```

如果是 windows 系统，环境搭建好后可以运行项目下的`cli.bat`快速启动

### 项目配置

1. 如果使用自己的域名，`CNAME`文件里的内容请换成你自己的域名，然后 CNAME 解析到`用户名.github.com`
2. 如果使用 GitHub 的的域名，请删除`CNAME`文件,然后把你的项目修改为`用户名.github.io`
4. 修改`_config.yml`文件，具体作用请参考注释
5. 清空`post _posts`目录下所有文件，注意是清空，不是删除这两个目录
6. 网站的 logo 和 favicon 放在了`static/img/`下，替换即可，大小无所谓，图片比例最好是 1:1
7. 如果你是把项目 fork 过去的，想要删除我的提交记录可以先软重置到第一个提交，然后再提交一次，最后强制推送一次就行了

### 使用

文章放在`_posts`目录下，命名为`yyyy-MM-dd-xxxx-xxxx.md`，内容格式如下

```
---
layout: mypost
title: 标题
categories: [分类1, 分类2]
---
文章内容，Markdown格式
```

文章资源放在`posts`目录，如文章文件名是`2019-05-01-theme-usage.md`。
