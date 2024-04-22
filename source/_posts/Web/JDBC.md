---
title:
  "{ title }": 
date:
  "{ date }": 
author: Blake
img: 
top: false
hide: false
cover: false
toc: false
summary: 
description: 
categories: 
tags:
---
# 简介
含义java数据库连接，是sum公司写的一套操作**关系型**数据库的API，一套接口
各个数据库厂商自己实现接口，提供数据库驱动jar包
使用APi编程，真正执行的代码是jar包中的实现类
用一套API就可以操作，不同的数据库

# 使用

1. 创建项目，导入驱动jar包
	2. 选择JDK，及编译版本
2. 注册驱动：告诉这个项目用的驱动
3. 建立连接
4. 定义sql语句
5. 创建连接对象
6. 执行sql
7. 处理返回信息
8. 释放资源
