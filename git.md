# Git是目前世界上最先进的分布式版本控制系统。
    git 常用命令的收集以及总结 
## 工作原理/流程
    ![image](https://github.com/zhouqinglong520/GitOrder/image/1.jpg)
## 名词
    1.master: 默认开发分支  
    2.origin: 默认远程版本库  
    3.Index / Stage：暂存区  
    4.Workspace：工作区  
    5.Repository：仓库区（或本地仓库）  
    6.Remote：远程仓库  

## 一、配置身份
    Git的设置文件为.gitconfig，它可以在用户主目录下（全局配置），也可以在项目目录下（项目配置）。  
    1.显示当前的Git配置  
       $ git config --list  
    2.编辑Git配置文件  
       $ git config -e [--global]  
    3.设置提交代码时的用户信息  
       $ git config [--global] user.name "[name]"    
       $ git config [--global] user.email "[email address]"  

## 二、新建代码库
    1.在当前目录新建一个Git代码库
      $ git init
    2.新建一个目录，将其初始化为Git代码库
      $ git init [project-name]
    3.下载一个项目和项目的整个代码创建历史到本地仓库
      $ git clone [url]
## 三、查看/增加/修改/删除文件
   ### 1.查看
      1.查看git状态
         $ git status
      2.查看变更内容
         $ git diff
   ### 2.增加
      1.添加指定文件到暂存区
         $ git add [file1] [file2] ...
      2.添加指定目录到暂存区，包括子目录
         $ git add [dir]
      3.添加当前目录的所有文件到暂存区
         $ git add .
      4.添加更改文件，要求确认，对于同一个文件的多出变化，可以实现分次提交
         $ git add -p
   ### 3.修改
      修改文件，并且将这个改名放入暂存区
         $ git mv [file-original] [file-renamed]
   ### 4.删除
      1.删除工作区文件，并且将这次删除放入暂存区
         $ git rm [file1] [file2] ...
      2.停止追踪指定文件，但该文件会保留在工作区
         $ git rm --cached [file]
    

      
