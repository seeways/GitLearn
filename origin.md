## 远程仓库

### 创建SSH Key

```bash
$ ssh-keygen -t rsa -C "youremail@example.com"

Generating public/private rsa key pair.  # 生成密钥对 
Enter file in which to save the key (/root/.ssh/id_rsa):  # 保存路径
Enter passphrase (empty for no passphrase):   # 密码，默认空
Enter same passphrase again:   # 重复密码
Your identification has been saved in /root/.ssh/id_rsa.
Your public key has been saved in /root/.ssh/id_rsa.pub.
The key fingerprint is:
92:41:73:6d:ba:03:bf:36:f8:ab:a2:90:0c:9c:a1:85 youremail@example.com
The key's randomart image is:
+--[ RSA 2048]----+
|      o ..       |
| .   . o  o      |
|E..   .  o       |
|o.o   .o.        |
|oo    ooS.       |
|o.     .+        |
|o.     . o       |
| .  . . +        |
|  .. ..+oo       |
+-----------------+

```

### 关联远程仓库

```bash
git remote add origin git@github.com:git_username/repository_name.git
```

添加后，远程库的名字就是origin

### 取消关联远程库

```bash
git remote remove origin
```

### 查看远程库

```bash
git remote
```

### 查看远程库详细信息

如果没有相关权限，则看不到相关地址信息  

例如没有推送权限，则看不到push地址

```bash
git remote -v
```

### 推送到远程仓库

```bash
$ git push origin <branch-name>
```

`-u` 表示第一次推送master分支的所有内容,不过建议先clone在push，尽量避免此方法

```bash
$ git push -u origin <branch-name>
```

日常提交只需要使用`git push`即可

### 从远程克隆

```bash
$ git clone https://github.com/usern/repositoryname.git
```

日常获取只需要使用`git pull`即可