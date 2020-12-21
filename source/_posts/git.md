---
title: My Git Cheat Sheet
date: 2020-12-21 23:02:22
tags: git
---

# Git cheat sheet

<img src="https://i.loli.net/2020/12/21/WFAHh2zlrnevmR6.png" alt="img" style="zoom: 67%;" />

<img src="https://i.loli.net/2020/12/21/bQPrOMFZ8vVNahX.png" alt="image-20201221214715280" style="zoom: 30%;" />

![img](https://www.runoob.com/wp-content/uploads/2015/02/git-command.jpg)

#### 添加删除文件

`git add . ` //添加所有文件

```
git add . //添加所有文件
```

```
git rm <file>
```




#### commit

```
git commit -m "提交说明"
```



#### push & pull



```
git pull
```




```
git push
git push -u <remote repo> <remote branch> // -u关联br
```



#### 远程仓库

```
git remote add <remote repo name> <git link>
```



#### branch

```
git checkout <branch>
```

```
git branch -d/--delete <branch>
```

删除远程分支：

```
git push origin --delete <branch> 
```

删除与远程分支的联系：

```
git branch --delete --remotes <origin>/<branch>
```



#### 回退

[git reset 命令](https://www.runoob.com/git/git-reset.html)



```
git reset
```

`git reset --soft HEAD^`：将最近一次提交节点的提交记录回退到暂存区

`git reset --mixed HEAD^`：将最近一次提交节点的提交记录回退到工作区

`git reset --hard HEAD^`：将最近一次提交节点的提交记录全部清除



```
git revert
```

通过创建一个新的版本，这个版本的内容与我们要回退到的目标版本一样，但是HEAD指针是指向这个新生成的版本，而不是目标版本。

`git revert HEAD` ：撤销前一次 commit

`git revert HEAD^` ：撤销前前一次 commit

`git revert commit + (commit id)`： 撤销指定的版本，撤销也会作为一次提交进行保存。

<img src="https://i.loli.net/2020/12/21/hMnBPSjbkTFoys3.png" alt="img"  />

git revert是用一次新的commit来回滚之前的commit，git reset是直接删除指定的commit。



#### 记录

记录commit

```
git log
```

记录每一次命令

```
git reflog
```



