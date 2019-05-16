---
title: 如何将py文件打包成exe可执行文件
date: 2019-03-27 20:17:32
tags:
---


## 下载pyinstaller

---

*pyinstaler官网*
[下载pyinstaler](http://www.pyinstaller.org/downloads.html)


---

*下载安装后，将压缩文件解压缩在Python安装目录下，进入该文件：*

---

*该目录中含有setup.py，同时在cmd中进入该目录：*

---

*输入命令*

> python setup.py install

---

*看到“Finished processing dependencies for PyInstaller==3.3.dev0+41c426f6d”，即安装成功：*

---


## 使用pyinstaller打包py文件成exe程序	



*将cmd的目录切换至（命令：cd 文件路径(注意空格)）需要打包的py文件目录下：*

> pyinstaller -F spider.py


>常用参数说明：
–icon=图标路径
-F 打包成一个exe文件
-w 使用窗口，无控制台
-c 使用控制台，无窗口
-D 创建一个目录，里面包含exe以及其他一些依赖性文件
pyinstaller -h 来查看参数

---

## pyinstaller 改变生成exe程序的图标

>pyinstaller -F --icon=my.ico spider.py

*my.ico 是一个图标名，和当前的spider.py文件在同一个目录下*

---

*打包好的exe文件，在同目录的dist文件中：*

---


*参考链接*

>https://blog.csdn.net/lqzdreamer/article/details/77917493