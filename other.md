### 常用忽略文件

https://github.com/seeways/MyIgnore

### 配置别名

```bash
git config --global alias.<name> <git-name>
```

建议熟悉git命令后使用

```bash
# 设置别名
git config --global alias.unstage 'reset HEAD'

# 使用别名撤掉修改,实际执行git reset HEAD test.py
git unstage test.py
```

对长命令的别名尤其好用
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

使用效果git lg

![result](https://cdn.liaoxuefeng.com/cdn/files/attachments/00138492662982594cbd1a942114472aeeb5f0a502faed1000/0)

### 显示颜色

如果没有默认显示变更文件的颜色，推荐此选项

```bash
git config --global color.ui true
```

### git config

1. 配置Git的时候，加上--global是针对当前用户起作用的，如果不加，那只针对当前的仓库起作用。
2. 仓库的Git配置文件都在仓库.git/config文件中
3. 全局的Git配置文件放在用户主目录下的.gitconfig中(隐藏文件)
4. 如果想修改配置或者别名，直接修改或删掉即可


