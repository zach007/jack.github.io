---
layout: post
title:  "用docker学习新技术的乐趣"
date:   2018-08-09 00:15:18 +0800
categories: jekyll update
header-img: img/post-bg-universe.jpg
tag: jekyll, blog
---
## 你能学到什么
1. docker 是什么使用场景是什么 
2. docker 有什么用和学习成本
3. docker 常见的命令

## 背景
目前我已经用docker用了一些什么
- docker官方文档过了一遍，下面都能在官方文档中找到
    - 操作系统:ubuntu / centos 
    - 数据库: mongodb /  mysql / postgresql
    - 集群: 简单的nginx 集群  
- 自己玩的
    - 学习新语言 : haskell 镜像
    - 运维CI/CD : 建了jenkins + sonar + nexus 环境
    - 大数据 : hadoop 集群
    - 测试 : 用spock框架写测试用例等

## 正文
推荐阅读 [如何通俗易懂解释docker是什么]
简单的来说docker
- docker 是一种容器技术，简单的来说可以看作是一种虚拟机，但是比虚拟机启动速度更快。容器能容纳不同的环境/不同的应用的。
- docker 最大的优势是环境可描述，通过配置dockerfile,可以快速生成想要的环境
举例子说明,假设现在需要搭建一套CI/CD 工具链 sonar + nexus + jenkins ，传统的搭建方式[如何搭建持续集成环境],
这里来说相对比较简单，但是可以看出来依然相对恼人，首先不同不同应用都有不同命令和环境配置，管理起来相对耗时。假定有一个场景,
需要为每一个新员工本机搭建一个CI/CD的平台呢？ok,1000个人可能需要操作1000次，随着时间推移，有的环境需要升级新版本，假设500人，那么
原来的配置又需要重新配置，此时不同环境有不同的配置，管理更加混乱，如果换成docker来做呢，最简单只需要两步骤，jenkins为例
    1. 下载镜像 docker pull jenkins  
    2. 设置参数运行镜像 docker run -port 8080:8080 jenkins    
此时一个jenkins的环境已经配置好了，到这里为止，能docker能做什么呢，回到刚才的场景 1000人，我需要把命令或者将dockerfile(可以描述docker容器环境内容的文件)发送给1000人，让他们自行安装镜像，
而不用一个一个装，而且此时每个人都是相同的环境，如果需要升级，只需要修改dockerfile文件。
同时最重要的是，环境搭建非常快能让我们撇开细节，更容易投身在应用本身，我们关注的是jenkins而不是开始怎么搭建jenkins，`搭建环境本身并不能让你提高技术~`
假设今天有一个业务场景遇到瓶颈，例如java并发已经不能满足需求了，需要重新学习go语言的协程，并且重写，那么此时大可不必花费时间搭建go环境，可以重复上诉两个步骤:下载go镜像，设置参数运行go,接着关注在
go语言的语法特性上，是不是非常快咧(当然ide还是推荐vim/emacs)，是不是觉得很方便咧~
- docker 启动速度
docker启动速度相对虚拟机来说非常快，不用耗时在系统启停上
- docker 可以大规模部署，非常容易模拟和学习分布式集群，像我本身就搭建过多个节点的hadoop集群 等等。
- docker compose 
    在docker中，每一个容器都是相互独立的，意味着一个jenkins容器和sonar容器是独立的，那么如何让两者通讯呢,顾名思义 docker compose ，可以将两个容器组合在一起，组合成一个新的环境。
    docker compose file 也是用来描述docker环境的。
容器的最大产出是docker file
- dockerfile 可以用来描述环境，如果用vagrant管理虚拟机，那么对标的也有相应的描述文件 vagrantfile
- dockerfile 可以满足个性化自定义的需求
## 进阶
docker 网络
docker 持久化
谷歌 k8s
s
## 总结


[如何搭建jekyll博客]: https://www.jianshu.com/p/e68fba58f75c
[如何通俗易懂解释docker是什么]: https://www.zhihu.com/question/28300645
[如何搭建持续集成环境]: https://blog.csdn.net/lswnew/article/details/79193529

