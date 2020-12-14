---
title: VsCodeNodes
date: 2020-08-15 22:53:28
tags:
---
## vs 基本命令
行注释ctrl /
块注释shift alt a 
下方插入一行ctrl enter 
上方插入一行ctrl shift enter 
文件夹查找ctrl shift f 
格式化代码shift alt f 
代码行向左或向右缩进:   shift tab
切换到终端ctrl + ~ 
竖列选择alt shift 
生成假字lorem + tab 
查找替换 ctrl h  / ctrl f
打开文件夹 ctrl P
## npm
报错 npm安装的包的版本问题
## eslint
关闭eslint 在webpack的base.config下 注释掉eslint的相关配置即可
## vue 使用
vue init webpack my-project 用webpack初始化一个vue2项目
vue create myzhihu 创建一个vue3项目
vue ui 图形化创建
## git
1. 查看本机是否存在ssh cd ~/.ssh
2. 创建ssh ssh-keygen
3. 查看ssh cat ~/.ssh/id_rsa.pub
4. 添加到远程仓库 git remote add origin git@github.com:michaelliao/learngit.git
5.配置全局usename.useremail git config --global user.name "xxx" git config --global user.email "xxx@xxx"

git remote rm origin 删除远程仓库
git pull origin master 拉取远程仓库
git push -u origin master 推上远程仓库
git push -u origin +master 强制推送
git status 查看状态
//分支上传并合并
git pull
git checkout index-swiper 切换分支
...git push
git checkout master 切换到主分支
git merge origin/index-swiper 本地分支更新
git push 上传到远程的master
恢复本地删除的文件 git reset --hard

##cnpm
npm install -g cnpm -registry=https://registry.npm.taobao.org

##servers
ssh -p 22 root@115.159.123.70 登陆服务器
mkdir rmdir 创建删除目录
pwd 查看当前目录
mkdir key_backup$ cp id_rsa* key_backup$ rm id_rsa* 清除原有ssh
ssh-keygen -t rsa -C “您的邮箱地址” 生成ssh
cat id_rsa.pub 查看ssh
