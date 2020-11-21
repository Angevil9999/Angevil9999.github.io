---
title: Github中HEXO的上传同步与备份恢复
date: 2020-11-20 22:00:42
categories:
- hexo学习 # 分类
tags: hexo Github 备份 同步 # 标签
---
# Github的备份
> 1、建立Github仓库的分支
 ```
 git checkout -b hexo
 ```
<!-- more -->
> 2、安装`hexo-deployer-git`插件
 ```
 npm install hexo-deployer-git
 ```



> 3、与远程 Git 仓库建立连接（一次即可）

```
git remote add origin https://github.com/你的用户名/你的名字.github.io
```
> 4、制作脚本  
> 首先在我们本地的HEXO根目录下建立一个 `update.sh`文件  
> 内容为
```
info=$1
if ["$info" = ""];
then info=":pencil: update content"
fi
git add -A
git commit -m "$info" # 这里的info为本次更新的内容标签，可以不填写。
git push origin hexo
hexo g && hexo d
```
>保存后，执行
```
sh update.sh
```
> 等待一分钟左右的时间博客即可更新完成

> # 写在最后，  
> 本站所有教学知识点，均来源于 <font size=5 color=#108fff >云游君</font> 的指点， <font size=5 color=red >在此表示感谢!!!</font>  
> 他的群号为： <font size=5 color=#108fff > 389401003 </font>  ，博客地址在我的友情链接里有。