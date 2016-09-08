##  查看日志  ##

    1.查看提交日志：
    git log
    2. 只显示提交信息的第一行
    git log --pretty=short
    3. 只显示制定目录，文件的日志
    git log README.md
    4. 显示文件的改动
    git log -p 
    5. 以图表形式显示
    git log --graph
    6. 查看当前仓库执行过的操作的日志
    git reflog 

###  查看更改前后的差别  ###

    1.查看工作树和暂存区的差别
    git diff
    2. 查看工作树和最新提交的差别
    git diff HEAD


### 创建分支： ### 

    1. git checkout -b fix-B
    合并至master分支
    2. git merge --no-ff master
    
    3. git push --set-upstream origin fix-B



> 当前分支推送到远程master  

- git push -u origin master 
 

> 推送至master以外的分支   
 
- git push -u origin feature-B
 
### 从远程仓库获取 ###

    获取远程仓库
     git clone git@github.com:Tanshixiong/MyGitHub.git 
     
    获取远程的feature-D分支
    git checkout -b feature-D origin/feature-D 
     
     
 
 
 
 
 
 
 
 
 
 
 
 
 
 
