## Remote Repository

### Create SSH Key

```bash
$ ssh-keygen -t rsa -C "youremail@example.com"

Generating public/private rsa key pair.  # Generate key pair
Enter file in which to save the key (/root/.ssh/id_rsa):  # Save path
Enter passphrase (empty for no passphrase):   # Password, leave blank for no passphrase
Enter same passphrase again:   # Repeat password
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

### Associate with a Remote Repository

```bash
git remote add origin git@github.com:git_username/repository_name.git
```

After adding, the remote repository will be named "origin."

### Remove Association with a Remote Repository

```bash
git remote remove origin
```

### View Remote Repositories

```bash
git remote
```

### View Detailed Information of Remote Repositories

If you don't have the relevant permissions, you won't see the address information.

For example, if you don't have push permission, you won't see the push address.

```bash
git remote -v
```

### Push to a Remote Repository

```bash
$ git push origin <branch-name>
```

`-u` is the same as `--set-upstream` and is used to associate the local branch with the remote branch.

```bash
$ git push -u origin <branch-name>
```

For regular submissions, you can simply use `git push`.

### Clone from a Remote Repository

```bash
$ git clone https://github.com/usern/repositoryname.git
```

For regular updates, you can simply use `git pull`.