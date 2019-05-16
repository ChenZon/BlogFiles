---
title: 在github上搭建个人博客
date: 2019-03-13 17:25:10
tags:
---

**闲着没事,就自己捣鼓一下,探究如何在github上搭建自己个人的博客**
**建立自己个人博客网站的好处:** 
**1.把平时积累的知识记录下来,以便日后查看复习** 
**2.更好的熟练git(捂脸)** 
**3.向个位大佬齐(敬礼)** 

---
## 准备工作




*在github上创建仓库*
[创建仓库](https://github.com/new)

---

*安装git*
[下载git](https://git-scm.com/download/)

---

*使用SSH将git与Github进行绑定*
[window进行配置](https://blog.csdn.net/zero________________/article/details/81143284)
[linux进行配置](https://blog.csdn.net/dong_W_/article/details/78787162)


---

*安装node.js*
[下载node.js](https://nodejs.org/en/download/)

---

*安装hexo*
> $npm install -g hexo-cli


---

## 生成项目


>&nbsp;$hexo init <folder\>  &nbsp;&nbsp;&nbsp;&nbsp;#folder为你存储项目的文件夹
>&nbsp;$ cd <folder\>
>&nbsp;$ npm install
>&nbsp;$ hexo generate  #或hexo g  
>&nbsp;$ hexo server    #或hexo s  启动本地服务器,然后可以通过http://localhost:4000 访问

## 部署到github
*在项目里找到_config.yml文件*
>deploy:
>    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;type: git  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#注意":"后有空格
>    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;repo: git@github.com:ChenZon/ChenZon.github.io.git  &nbsp;&nbsp;&nbsp;#域名填写你本人的
>    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;branch: master  


*回到命令行，输入以下命令*
>&nbsp;$npm install hexo-deployer-git --save
&nbsp;$hexo generate #或hexo g
&nbsp;$hexo deploy   #或hexo d

*然后可以正常通过域名访问刚刚所部署的项目*

**https://chenzon.github.io** #访问本人的github地址

## 更换主题
*如果你觉得主题不好看，可以根据自己的爱好进行更换*
**https://hexo.io/themes/**

---

*当你看上了喜欢的主题，将其下载到本地*

>$git clone git@github.com:blinkfox/hexo-theme-matery.git #注意：要下载到项目中的themes文件里


*在项目里找到_config.yml文件，作以下修改*

>theme: hexo-theme-matery &nbsp;&nbsp;&nbsp;#hexo-theme-matery为你所下载的主题名字

*然后重新部署*

>&nbsp;hexo clean &nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;hexo generate &nbsp;&nbsp;&nbsp;&nbsp;#或hexo g
&nbsp;hexo deploy &nbsp;&nbsp;&nbsp;&nbsp;#或hexo d

