---
layout: post
title:  "Welcome to Jekyll!"
date:   2018-08-09 00:15:18 +0800
categories: jekyll update
header-img: img/post-bg-universe.jpg
tag: jekyll, blog
---
## 你能学到什么
1. 如何搭建个人博客
2. 为什么选择jekyll 
3. 简单使用jekyll

## 背景
今天开始写博客，感觉会有一些东西想跟大家分享一下，毕竟分享也是成长的一部分。  
昨晚开始搭建博客系统，选择了jekyll的原因有
- 静态博客，马上能看见效果，调试方便
- jekyll理念，官网宣称的，让作者忘记主题，关注产出(post文章)。
- 支持 `makedown` 格式  

## 正文
1. 先推荐各位使用linux，因为是官方推荐系统，jekyll会依赖`ruby` ,linux下安装起来会比较简单，
windows10的话可以开启虚拟化，有自带的ubuntu也是可以的。  
windows安装会比较麻烦，首先安装ruby，其次要设置Path等等比较麻烦，而且会中文乱码，windows下推荐使用安装包管理`chocolatey`工具  
当然最推荐的是docker，因为我最不喜欢就是搭建环境，这是时间收益比最低的地方啦。  
**`所以下一篇文章会写到docker，和大家分享一个用docker学习新技术的套路`**
2. 我是fork了这个人项目入门的，如果有兴趣可以看一下 [如何搭建jekyll博客]
3. 简单的说明一下jekyll文件结构(只关注重点)
  - posts : 博客文章
  - layouts : 页面布局
  - other : 不用管
4. 简单的介绍一下jekyll命令
   1. jekyll new path : 新建文章
   2. cd path ,bundle install : 安装插件
   3. bundle exec jekyll --watch : 运行jekyll,并且自动页面修改会自动刷新
   
## 总结
有很多想分享的，但是别人已经很详细了，倒不如给一个概念，然后谷歌一下方便快捷得多  
写文章真的是比我想象中耗费时间呀，当作草稿慢慢写好了。。。

[如何搭建jekyll博客]: https://www.jianshu.com/p/e68fba58f75c

