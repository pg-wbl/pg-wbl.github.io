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
categories: JavaWeb
tags:
  - MyBatis
---
# 简介

## 04解决sql语句警告提示
原因：IDEA没有识别到数据库
解决：将数据库关联到IDEA中
- 找到位置
![image.png](https://i0.hdslb.com/bfs/article/7e705596c3e63c99c612d8366a8ee0f3441011616.png)
- 新建数据源
![image.png](https://i0.hdslb.com/bfs/article/65ab43b0d1ce3e6e1646e51847b871fb441011616.png)
- 配置
![image.png](https://i0.hdslb.com/bfs/article/01629a1ee248cdffeb8750e33e14373a441011616.png)
- 直接对数据库进行查询操作
![image.png](https://i0.hdslb.com/bfs/article/7fbdef4126b9085e4ede65e4adbd650a441011616.png)

# Mapper代理开发
