---
title: Github中HEXO的上传同步与备份恢复
date: 2020-11-20 22:00:42
categories:
- hexo学习 # 分类
tags: hexo Github 备份 同步 # 标签
---
# Github的备份
## 1、建立Github仓库的分支
> ```
> git checkout -b hexo
> ```
<!-- more -->
##  2、安装`hexo-deployer-git`插件
> ```
> npm install hexo-deployer-git
> ```
##  3、与远程 Git 仓库建立连接（一次即可）
> ```
> git remote add origin https://github.com/你的用户名/你的名字.github.io
> ```
##  4、制作脚本  
> 首先在我们本地的HEXO根目录下建立一个 `update.sh`文件  
> 内容为
> ```
> info=$1
> if ["$info" = ""];
> then info=":pencil: update content"
> fi
> git add -A
> git commit -m "$info" # 这里的info为本次更新的内容标签，可以不填写。
> git push origin hexo
> hexo g && hexo d
> ```
> 保存后，执行
> ```
> sh update.sh
> ```
> 等待一分钟左右的时间博客即可更新完成

# Github的恢复
## 第一步
### 远程克隆位于Github的仓库（之前我们备份到分支的仓库）
> 运行命令
>
> ```
> git clone -b hexo https://github.com/XXX/XXX.github.io.git
> ```
>
> 克隆你仓库中的分支，分支名为（hexo）
>
> 输入`PWD`查看所在目录
## 第二步
### 在新电脑上安装依赖
>1、安装`nodejs`
>```
>sudo apt-get install nodejs
>sudo apt-get install npm
>```
>
>2、安装`git`
>
>```
>sudo apt install git-all
>```
>
>3、安装`hexo`
>
>```
>npm install hexo-cli -g
>```
>
>如果安装出错请执行
>
>```
>sudo npm install hexo-cli -g
>```
## 第三步
>### 运行测试
>完成以上步骤后输入
>```
>hexo s
>```
>测试网站是否可以顺利运行

