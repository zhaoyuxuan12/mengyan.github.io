---
layout: post
title: Git 命令
tag: 博客
---

# Github
[TOC]
## 安装git

1.sudo apt-get install git 安装git
2.git config --global user.name " " 创建名
3.git config --global user.name " " 创建邮箱

## 创建版本库

1. 创建路径
	- mkdir learngit 创建路径
	- cd learngit 进入路径
	- pwd 显示当前目录

2. 管理仓库
	- git init 把目录变成管理仓库 初始化仓库
	- 创建一个readme.txt文件
	- git add readme.txt 把文件添加到仓库
	- git commit -m "wrote a readme file" 把文件提交到仓库
	- 也可以提交多个文件
		- git add file1.txt
		- git add file2.txt
		- git commit -m "add 3 files." 

## 时光穿梭

1. 修改提交
	- 修改readme.txt文件
	1. git status 查看结果
	2. git diff 查看修改的内容
	3. git add readme.txt 把文件添加到仓库
	4. git commit -m "add distributed" 把文件提交到仓库
	5. git status 查看当前状态

2. 版本退回
	1. git log 查看历史文档版本
	- git log --pretty=oneline 缩短查询的历史版本 视觉上简化
	2. git reset --hard HEAD^ 退回上一个历史版本 HEAD代表本版本 HEAD^上一个版本 HEAD^^ 代表上一个版本 HEAD~100 第100个版本
	3. git rest --hard 1094a 退回id是1094a……的版本
	4. git reflog 记录你的每一次命令

3. 工作区和暂存区
	1. git add 是将文件存到暂存区。
	2. git commit -m 是将文件提交到分支进行保存

4. 管理修改
	1. 在工作区修改1.txt然后git add 添加后在修改1.txt 后git commit -m 提交后提交的是第一次修改文件。 第二次的并没有提交 需要再次提交。
	2. cat 文件 可以查看文档内容
	3. git diff HEAD -- 文件名和后缀名 可以查看工作区的和版本库里面最新版本的区别文本爱暂存的时候用