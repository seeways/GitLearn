## Version Control

### 初始化一个Git仓库

```bash
$ git init
```

### 添加文件到Git仓库

```bash
$ git add <file>
$ git commit -m "description"
```
`git add`可以反复多次使用，添加多个文件，`git commit`可以一次提交很多文件，`-m`后面输入的是本次提交说明。


### 添加全部修改到暂存区

```bash
git add -A .
```

- `git add -A`表示添加所有内容
- `git add .` 表示添加新文件和编辑过的文件不包括删除的文件
- `git add -u` 表示添加编辑或者删除的文件，不包括新添加的文件。

### 查看工作区状态

```bash
$ git status
```

### 查看修改内容

- `git diff` 查看工作区(work dict)和暂存区(stage)的区别
- `git diff --cached` 查看暂存区(stage)和分支(master)的区别
- `git diff HEAD -- <file>` 查看工作区和版本库里面最新版本的区别

### 版本回退

```bash
$ git reset --hard HEAD^
```

以上命令是返回上一个版本，在Git中，用`HEAD`表示当前版本，上一个版本就是`HEAD^`，上上一个版本是`HEAD^^`，往上100个版本写成`HEAD~100`。

### 回退指定版本号

```bash
$ git reset --hard commit_id
```
commit_id是版本号，是一个用SHA1计算出的序列

### 放弃暂存区修改

1. 退回工作区

```bash
$ git reset HEAD <file>
```

2. 撤销工作区的修改

```bash
$ git checkout -- <file>
```

Tip：
1. 当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令`git checkout -- <file>`。
2. 当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令`git reset HEAD <file>`，就回到了第一步，第二步按第一步操作。
3. 已经提交了不合适的修改到版本库时，想要撤销本次提交，进行版本回退，前提是没有推送到远程库。

### 很重要的git checkout注意点
`git checkout -- file`命令中的`--`**很重要！很重要！很重要！**，没有`--`，就变成了**切换到另一个分支**的命令

