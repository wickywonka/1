---
layout: post
title: '使用Jekyll和GitHub Pages搭建个人博客'
date: 2018-01-29
author: 王维
tags: 个人教程
---
## 　 前言
　　从什么时候开始有这种想法的呢？大概是网易博客无故被封转战新浪博客，又觉得新浪博客的编辑器十分难用时产生的。<br>
　　至于为什么想法搁置了４个月，原因多种多样，一是因为我懒，二是博客这个东西没有走入我的生活中。但我是一个爱好比较广泛的人，在不断的尝试新鲜事物时，各种问题也接踵而至，兴趣加问题产生动力，在尽我所能解决掉问题时，一种激动而愉悦的心情油然而生，然而只能自己一个人暗爽，总不能拉着人讲个不停，那样脸皮未免也太厚了不是？在与博客不断的接触后我就萌生了一种想法，既然不愿意一个人暗爽，又不能拉着别人嘚啵个不停，那就写成博客，用文字记录下来吧。<br>
*我的个人博客地址：http://blog.wonka.top/* <br>
*个人博客的代码仓库：https://github.com/wickywonka/wickywonka.github.io ，可做模板克隆并修改成自己的博客* <br>
## 　基本过程
* 安装Ruby
* 更改Ruby默认的source源
* 安装Jekyll
* 安装bundle
* 安装GitHub desktop
* 注册GitHub账号并建立GitHub pages
* 将GitHub pages仓库克隆到本地
* 克隆一份主题模板覆盖到本地仓库&修改模板
* 写博文并检查
* 将博文从本地推送到远端
* 购买域名并绑定到GitHub pages（可选）
## 详细步骤 
#### 安装Ruby 
　　Ruby可在http://rubyinstaller.org/downloads/下载，建议下载2.4.x版本，不要下载2.5版本。安装时记得把 *Add Ruby executables to your PATH* 勾上来配置环境变量。<br>
安装后，可在cmd中输入`ruby -v`和`gem -v`来查看版本号看是否安装成功<br>
#### 更改Ruby默认的source源
　　由于官方源速度太慢，在cmd中依次输入以下代码来更改速度更快的源<br>
　　`gem sources -r https://rubygems.org/ ` <br>
　　`gem sources -a http://gems.ruby-china.org` <br>
#### 安装Jekyll
　　在cmd中输入以下代码来安装Jekyll <br>
　　`gem install jekyll` 
#### 安装bundle
　　在cmd中输入以下代码来安装bundle <br>
　　`gem install bundler`
#### 安装GitHub desktop
　　GitHub desktop可在https://desktop.github.com/下载 
#### 注册GitHub账号并建立GitHub pages&将GitHub pages仓库克隆到本地
　　首先到https://github.com/注册GitHub账号，然后参考GitHub pages官方文档https://pages.github.com/建立GitHub pages，并将其克隆到本地，GitHub pages的地址一般为“GitHub账号用户名.github.io”
#### 克隆一份主题模板覆盖到本地仓库&修改模板
　　可以在http://jekyllthemes.org/选择自己喜欢的主题模板克隆，也可以克隆我的或者克隆我博客主题原作者的https://github.com/kaeyleo/jekyll-theme-H2O，主题名为h2o，推荐此主题，作者是个国人，有中文说明文档，方便按照修改
#### 写博文并检查
　　打开本地仓库文件夹，有一个名为_posts的文件夹，要发表的博文都要放在这里，文件名称格式为“年-月-日-博客名称.md”，如2018-01-01-Hello World.md <br>
　　书写博客使用markdown语言，可以阅读官方文档进行学习，markdown语言十分简单，可以迅速学会，官方文档的地址为http://wowubuntu.com/markdown/<br>
　　写完后使用cmd并跳转到本地仓库路径，输入以下代码<br>
`jekyll s` <br>
　　然后就可以在浏览器中输入http://127.0.0.1:4000/，来检查自己的博客在正式的网站上是什么样子，没问题后就可以从本地推送到远端
#### 将博文从本地推送到远端
　　在本地仓库更改或添加文件后，GitHub desktop的changes一列就会显示出来，在填写summary和description后点击commit and master，然后再点击fetch origin就完成推送了，然后就去GitHub pages欣赏你的博文吧
#### 购买域名并绑定到GitHub pages（可选）
　　一个独特的域名可以使你的博客更有辨识度，域名可在阿里万网上购买，.top域名第一年只需要3元，3年三十多，但是需要实名认证，像.com等这种顶级域名还需要备案，也可在godaddy上购买，一个新加坡域名售卖网站，不需要实名认证，有中文，支持支付宝<br>
　　域名购买后在本地仓库根目录新建文本文档，输入你购买的域名，重命名为CNAME，注意大写，没有后缀名，然后推送到远端<br>
　　然后ping一下GitHub pages地址，得到自己主页的ip，然后到域名管理后台添加解析，万网和godaddy做法不一样，具体如何添加，可自己百度了解
### 总结
　　用Jekyll和GitHub pages搭建博客的基本教程到这就结束了，如果在搭建过程中遇到问题，多百度，多看别人的博客，最重要的多看官方文档，基本上都能解决，最后，祝大家搭建顺利。