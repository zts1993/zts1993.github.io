---
layout: post
title: 怎样检查自己的某个端口是否被占用
date: 2016-02-18 13:12:52  +0800
categories: 记录
---

用惯了netstat回windows有点不适应

开始,运行,输入cmd,在命令提示符输入netstat -ano   然后在local Address那列找出你要找的端口,比如找到有127.0.0.1:80(冒号后面就是端口号),说明这个端口已经被占用了.  
再看这行后面的pid号,记住它  
然后打开任务管理器(Ctrl+Alt+Delete),点菜单里的"查看",点"选择列(s)...",在里面把"PID(进程标识符)"前面钩上,然后就可以在进程列表中找出你刚才记住的pid号,其相对应的进程你也找到了,  你可以做结束改进程的操作来释放这个端口.  