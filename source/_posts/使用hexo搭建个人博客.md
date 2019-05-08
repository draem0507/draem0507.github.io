title: 使用hexo搭建个人博客
author: draem0507
date: 2019-05-06 22:20:28
tags:
---

# 引言
> 博主之前使用第三方博客平台，例如CSDN，博客园等进行博客撰写；后面有尝试使用jeklly，最近发现hexo更适合；因此本文重点讲述hexo的搭建及其在使用中的一些心得。
# hexo介绍
[hexo](https://hexo.io/zh-cn/)是一个快速、简洁且高效的博客框架。具有一键部署、快速渲染的特点；支持markdown语法，还拥有丰富的插件。
## hexo的使用
通过以下命令，可以快速完成hexo的安装、部署和启动
``` bash
$ npm install hexo-cli -g
$ hexo init blog
$ cd blog
$ npm install
$ hexo server
```
前提条件：本地事先安装好git、npm等环境

<!--more-->

## 安装教程
[详细安装说明](https://easyhexo.com/1-Hexo-install-and-config/)



# hexo发布
如果不想每篇文章都重复的调用 生成、发布等动作；那么以下工具可以提升我们的工作效率

## hexo-admin

hexo-admin是hexo的管理后台；类似于传统的文章管理后台，集成文章的创建、修改、发布等功能

* [hexo-admin 配置传送门1](https://www.jianshu.com/p/68e727dda16d)
* [hexo-admin 配置传送门2](https://blog.csdn.net/smileyan9/article/details/86666824)
* [Browsersync 浏览器实时更新插件](https://github.com/hexojs/hexo-browsersync)

## travis
> [travis](https://www.travis-ci.org/) 一款免费好用的CI工具；通过项目库(例如github)关联后，每次提交代码，都可以自动触发编译，实时将最新的博客内容生成到个人主页上。对于一些敏感的信息，可以通过travis管理，而不用直接暴露在hexo的配置文件中。


* [travis 配置传送门1](https://blog.csdn.net/daye5465/article/details/77118886)
* [travis 配置传送门2](https://www.jianshu.com/p/5691815b81b6)

# 周边
## 编辑器
* [markdown语法介绍](https://blog.csdn.net/zhuzhuyule/article/details/58347687)
* [HexoEditor](https://github.com/zhuzhuyule/HexoEditor)


## 插件

* [评论插件介绍](https://www.jianshu.com/p/7e4453421b8f)
* [博主使用的评论插件  Valine](https://ioliu.cn/2017/add-valine-comments-to-your-blog/)

## 主题
* [知乎：好看点hexo 主题：](https://www.zhihu.com/question/24422335)
* [hexo-theme-next](https://github.com/theme-next/hexo-theme-next)



## 代码管理
* source与master：使用master作为发布分支；另外创建一个博客源文件的分支，用于编辑md文件
* [.gitmodules](https://blog.csdn.net/hzhj2007/article/details/79917059) 当我们使用hexo的主题的时候，可以通过gitmodules来完成动态编译工作，保证实时获取到最新版本的主题

# 问题FAQ

**建 hexo，在执行 hexo deploy 后,出现 error deployer not found:github 的错误**
> npm install hexo-deployer-git --save  

 如果提示安装失败，可以切换到root命令执行 sudo -iu root，然后重新deploy

**Hexo下Next主题生成静态文件时报错no such file or directory, open themes\next\layout\_scripts\schemes\.swig**
> 利用工具 YAML Validator 检查 站点配置文件 主题配置文件 _config.yml

**Angular macOS Err:EACCES: permission denied**
>[解决办法](https://www.jianshu.com/p/60b3d5584afe)


# 参考
[Doublemine](https://github.com/Doublemine/Doublemine.github.io/tree/source)