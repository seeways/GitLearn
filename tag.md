## 标签
tag就是一个让人容易记住的有意义的名字，它跟某个commit绑在一起。

### 新建一个标签

```bash
$ git tag <tagname>
```

命令`git tag <tagname>`用于新建一个标签，默认为HEAD，也可以指定一个commit id。

### 指定标签信息

you can use like this: `git tag -a <tagname> -m "say something..."`

```bash
$ git tag -a <tagname> -m <description> <branchname> or commit_id
```


### PGP签名标签

you can use like this: `git tag -s <tagname> -m "say something..."`

```bash
$ git tag -s <tagname> -m <description> <branchname> or commit_id
```

### 查看所有标签

```bash
$ git tag
```

### 推送一个本地标签

```bash
$ git push origin <tagname>
```

### 推送全部未推送过的本地标签

```bash
$ git push origin --tags
```

### 删除一个本地标签

```bash
$ git tag -d <tagname>
```

### 删除一个远程标签

```bash
$ git push origin :refs/tags/<tagname>
```
