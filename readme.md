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

###### 分支

- 创建分支 `git branch dev`
- 查看分支 `git branch`
- 切换分支 `git checkout dev`
- 合并分支 `git merge dev`
- 删除分支  `git branch -d dev`

###### 远程服务提交

+ 提交代码到远程 `git push https://www.baidu.com` 
+ 更新代码到本地 `git pull https://www.baidu.com`
+ 从服务器检出代码   `$ git clone www.baidu.com`

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