---
title: 开启Github云端保存VScode各项配置的方法
date: 2020-11-23 20:04:04
categories: # 分类
- hexo学习 
tags: Github VScode # 标签
---
# 开启**Github**云端保存VScode各项配置的方法
## 第一步
>1.首先在`Github.com`中登录需要保存配置文件的账号；  
> 2. 点击头像，选择`settings`进入设置；  
> 3. 在新页面中右边栏中选择`Developer settings`；  
> 4. 接下来进入`Personal access tokens`选项中；  
> 5. 记录`Personal access tokens`中的密钥，此处的密钥需要保存好，在新的机器中下载配置文件时需要用到。
## 第二步
> 1. 在VScode中搜索插件`settings sync`并安装；   
> 2. 在插件的页面  

windows快捷键
 <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>D</kbd>  
Mac快捷键
 <kbd>Shift</kbd> + <kbd>Option</kbd> + <kbd>D</kbd>
 
> 3. 在新页面中选择`EDIT CONFIGURATION`并输入第一步中记录下来的密钥！  
 这时就已经设置好了上传同步的设置

## 第三步

> 1. 在新的电脑上重复上面的步骤，在第二部同步快捷键改为下面的

windows快捷键
<kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>U</kbd>  
Mac快捷键
 <kbd>Shift</kbd> + <kbd>Option</kbd> + <kbd>U</kbd>
 
> 2. 此时新电脑上将开始下载之前的配置并应用。