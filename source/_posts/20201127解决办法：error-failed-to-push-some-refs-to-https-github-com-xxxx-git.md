---
title: >-
  解决办法：! [rejected]        master -> master 
  'https://github.com/xxxx.git
date: 2020-11-27 17:00:12
tags: 学习 # 标签
categories:
- 问题解决方案 # 分类
---

# 1、问题
> ### 在github远程创建仓库后, 利用gitbash进行提交本地文件的时候出现如下错误：

```
$ git push -u origin master
To git@github.com:***.git
! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:***.git
hint: Updates were rejected because the tip of your current branch is behin
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
# 2、分析
> ### git仓库中已经有一部分代码，所以它不允许你直接把你的代码覆盖上去。
# 3、解决方法  
> ### 方法1：强行将代码推到github仓库里面去
 ```
 git push -f origin master
 ```
> 直接强推，即利用强覆盖方式用你本地的代码替代github仓库内的内容。  
> 如果是分支，将命令中`master`改为分支名称即可。