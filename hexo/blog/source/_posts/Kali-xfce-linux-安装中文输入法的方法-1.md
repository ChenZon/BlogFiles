---
title: Kali(xfce) linux 安装中文输入法的方法
date: 2019-04-02 08:00:36
tags:
---


** 本来挺简单的一件事，拖了这么久，实在惭愧。。。**
** 首先我的是Kali-linux(基于xfce主题)**

---

### 在终端输入下面的命令

>$ leafpad /etc/apt/sources.list   #用编辑器打开sources.list

---

### 将sources.list文件清空，然后加入下面信息，即保存一个阿里云的下载源

> deb http://mirrors.aliyun.com/kali kali-rolling main non-free contrib

---

### 然后在终端输入下面命令

>$ apt-get update  
这个命令会访问源列表里的每个网址，并读取软件列表，然后保存在本地电脑。我们在新立得软件包管理器里看到的软件列表，都是通过update命令更新的。update后，可能需要apt-get upgrade一下。

---

### 执行下面指令
>$ apt-get install fcitx fcitx-googlepinyin

---

### 然后在配置里设置输入法，选择Google拼音即可

---

### 参考链接

> https://blog.csdn.net/mars_guest/article/details/79899202
