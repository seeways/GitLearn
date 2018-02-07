## 分支

### 创建分支

```bash
$ git branch <branchname>
```

### 查看分支

all branch

```bash
$ git branch
```

### 切换分支

```bash
$ git checkout <branchname>
```

### 创建+切换分支
```bash
$ git checkout -b <branchname>
```

### 合并某分支到当前分支

```bash
$ git merge <branchname>
```

### 删除分支

```bash
$ git branch -d <branchname>
```

### 查看分支合并图

**当Git无法自动合并分支时，就必须首先解决冲突。** 解决冲突后，才可以继续操作。

```bash
$ git log --graph
```

### 普通模式合并分支

```bash
$ git merge --no-ff -m "description" <branchname>
```

因为本次合并要创建一个新的commit，所以加上`-m`参数，把commit描述写进去。  

合并分支时，加上`--no-ff`参数就可以用普通模式合并，能看出来曾经做过合并，包含作者和时间戳等信息，而fast forward合并就看不出来曾经做过合并。

### 保存工作现场

```bash
$ git stash
```

### 查看工作现场

```bash
$ git stash list
```

### 恢复工作现场

```bash
$ git stash pop
```

### 丢弃一个没有合并过的分支

```bash
$ git branch -D <branchname>
```

### 查看远程库信息

```bash
$ git remote -v
```

### 在本地创建和远程分支对应的分支

建议本地和远程分支的名称保持一致

```bash
$ git checkout -b branch-name origin/branch-name，
```


### 建立本地分支和远程分支的关联

```bash
$ git branch --set-upstream branch-name origin/branch-name；
```

### 从本地推送分支

如果推送失败，先用`git pull`抓取远程的新提交；

```bash
$ git push origin branch-name
```


### 从远程抓取分支

如果有冲突，要先处理冲突。

```bash
$ git pull
```