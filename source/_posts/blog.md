---
title: blog
date: 2020-08-15 11:37:55
tags:
---
## Creat Hexo cli
- npm install -g hexo-cli
- hexo init hexo-blog
- cd hexo-blog
- code .
## _config
- language: zh-CN
## themes
- git搜索hexo-theme
- git clone 主题    //git clone https://github.com/probberechts/hexo-theme-cactus.git themes/cactus
- 文件夹打开主题 删除.git 删除默认主题
- _config 找到theme 改名 运行看是否生效 修改主题颜色 找到colorscheme
## Instakk yarn
- git init
- git remote add origin git@github.com:XiaoJiaHu/xiaojiahu.github.io.git
- npm install -g yarn
- yarn add hexo-deployer-git  //hexo-deployer-git是一个依赖 库 帮生成好的代码部署到一个具体的分支
## Modify some files
- _config
  deploy:
  type: git
  repo:https://github.com/XiaoJiaHu/XiaoJiaHu.github.io
  branch: master    //如果使用的第二种方式 这里改为gh-pages
## deploy code to github
- hexo run deploy  \ hexo deploy     //github pages出现站点

# 自动化部署
## creat branch
- git add .
- git commit  
- git checkout -b myblog	 
    - git branch 显示分支
    - git branch -d myblog 删除一个分支
- git push --set-upstream origin myblog	  //将该分支push到github
## 继续
- 创建 .github / workflows / deploy.yml 这里面的代码见 https://github.com/objtube
- 注意最后的branch : master / folder : public   //这里可以add commit 看下 有 小圆点
## 编辑
- 打开themes / layout / post
- 底部增加一个div a 
- https://github.com/XiaoJiaHu/xiaojiahu.github.io/edit/myblog/source/_posts/blog.md 
        将_posts/blog.md  替换为<%- page.source %> 这个变量
## Follow-up
- hexo new fileName 	//创建一篇博客
- hexo remove fileName	//删除一篇博客
- hexo server           //打开本地连接