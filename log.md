
### 查看

```bash
$ git log
```

### 简化版日志

```bash
$ git log --pretty=oneline
```

### 查看前N条  

```bash
git log -n
```

### 变更日志

`-n` 同上,不加则显示全部

```bash
git log --stat -n
```

### 查看提交修改
查看某次commit做了哪些修改

```bash
git show <commit-hash-id>
```

### 退出log状态

有时候日志过长，可以按下英文q退出状态

### 查看提交历史和说明

```bash
$ git reflog
```