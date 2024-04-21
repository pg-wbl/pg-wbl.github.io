---
title: 使用Git
date: 2024-04-22 03:08:18
author: Blake
img: 
top: false
hide: false
cover: true
toc: false
summary: 
description: Git学习记录
categories: 工具
tags:
  - Git
---
# 本地
- Working tree （工作目录）：代码的存放位置

- Index（暂存区）：代码提交到仓库之前临时的存储空间

- Repository （本地历史仓库）：存放不同版本的代码


|    命令    |               作用               |
| :--------: | :------------------------------: |
|  git init  |       创建git仓库，初始化        |
| git status |           查看git状态            |
|  git add   |   添加，将指定文件添加到暂存区   |
| git commit | 提交，将暂存区文件添加到历史仓库 |
|  git log   |             查看日志             |
1. 初始化本地git仓库：git init
2. 添加文件：git add 文件名
3. 提交到暂存区：git commit -m '第一次提交'
4. 推送到远程仓库：git push -u 远程仓库名 分支名
	1. 查看远程仓库名：git remote -v

# 分支

| 命令                | 作用       |
| ----------------- | -------- |
| git branch 分支名    | 创建分支     |
| git checkout 分支名  | 切换分支     |
| git branch        | 查看已有分支   |
| ls                | 查看分支下的文件 |
| git merge 分支名     | 合并分支     |
| git branch -d 分支名 | 删除分支     |

- 切换分支：是将代码拉取到了本地工作目录

# 远程仓库

## SSH免密登录
1. 本地生成ssh公钥
- 

   1. 设置Git账户

| 命令                                   | 作用                   |
   | -------------------------------------- | ---------------------- |
  | git config user.name                   | 查看git账户            |
  | git config user.email                  | 查看git邮箱            |
   | git config --global user.name "账户名" | 设置全局账户名         |
  | git config --global user.email "邮箱"  | 设置全局邮箱           |
  | cd ~/.ss                               | 进入查看是否生成过公钥 |

  2. 生成公钥

   | 命令                        | 作用                         |
   | --------------------------- | ---------------------------- |
   | ssh-keygen -t rsa -C "邮箱" | 生成公钥，回车使用默认设置   |
  | cat ~/.ssh/id_rsa.pub       | 查看公钥，复制到仓库设置里面 |
   | ssh -T git@gitee.com        | 最后测试公钥                 |

 

  3. 设置账户公钥： cat ~/.ssh/id_rsa.pub  查看公钥，复制到仓库设置里面

  4. 公钥测试： ssh -T git@gitee.com（github.com）

   2. 将代码推送到远程仓库

   | 命令                                    | 作用                               |
   | --------------------------------------- | ---------------------------------- |
   | git remote add 远程仓库名称 远程仓库URL | 为远程仓库重命名（远程名称自定义） |
   | git push -u 远程仓库名称 分支名         | 推送到远程仓库                     |
   |                                         |                                    |

   3. 将远程仓库代码克隆到本地

   | 命令                            | 作用             |
   | ------------------------------- | ---------------- |
   | git clone 远程仓库地址          | 将代码克隆到本地 |
   | git push -u 远程仓库名称 分支名 | 推送到远程仓库   |