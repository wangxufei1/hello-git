# git使用文档

### 下载安装

> https://git-scm.com/downloads
>
> 安装完成后，在桌面，右键出现“Git Bash”就说明Git安装成功！

### 命令使用

###### 初始化: 

> `git init`

###### 创建用户名及邮箱：

> `git config --global user.name "wangxufei"`  
>
> `git config --global user.email "wangxufei668@163.com"`

###### 代码操作

- 新增代码   `git add <file>`   
- 删除文件   `git rm <file>`
- 提交代码   `git commit -m <message>`  --all 新增并提交
- 状态查看   `git status`
- 查看日志   `git log --oneline`
- 版本切换记录 `git reflog`
- 代码回滚   `git reset  --hard Head~0 |6282ab0`   
- 查看之前版本区别   `git diff HEAD -- readme.txt`
- 文件回到最近一次`git commit`或`git add`时的状态     `git checkout -- readme.txt`

###### 分支

- 创建分支 `git branch dev`
- 查看分支 `git branch`
- 切换分支 `git checkout dev`
- 合并分支 `git merge dev`
- 删除分支  `git branch -d dev`

###### 远程服务提交

+ 提交代码到远程 ` git push -u origin master` 
+ 更新代码到本地 `git pull `
+ 从服务器检出代码   `$ git clone www.baidu.com`
+ 增加远程连接   `git remote add origin git@github.com:michaelliao/learngit.git`

###### 冲突解决

```
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
<<<<<<< HEAD
Creating a new branch is quick & simple.
=======
Creating a new branch is quick AND simple.
>>>>>>> feature1
修改后重新提交：
$ git add readme.txt 
$ git commit -m "解决···冲突"
```
###### 多人协作

+ 首先，可以试图用`git push origin `推送自己的修改；
+ 如果推送失败，则因为远程分支比你的本地更新，需要先用`git pull`试图合并；
+ 如果合并有冲突，则解决冲突，并在本地提交；
+ 没有冲突或者解决掉冲突后，再用`git push origin `推送就能成功！