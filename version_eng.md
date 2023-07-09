## Version Control

### Initialize a Git Repository

```bash
$ git init
```

### Add Files to Git Repository

```bash
$ git add <file>
$ git commit -m "description"
```

You can use `git add` multiple times to add multiple files, and `git commit` to commit all the changes with a single message using the `-m` option.

### Add All Modifications to the Staging Area

```bash
git add -A .
```

- `git add -A` adds all changes.
- `git add .` adds new and modified files but does not include deleted files.
- `git add -u` adds modified or deleted files but does not include new files.

### View the Status of the Working Directory

```bash
$ git status
```

### View Modifications

- `git diff` shows the differences between the working directory and the staging area.
- `git diff --cached` shows the differences between the staging area and the latest commit.
- `git diff HEAD -- <file>` shows the differences between the working directory and the latest commit.

### Revert to Previous Version

```bash
$ git reset --hard HEAD^
```

The above command reverts to the previous version. In Git, `HEAD` represents the current version, `HEAD^` is the previous version, and `HEAD^^` is the version before that. To go back 100 versions, use `HEAD~100`.

### Revert to a Specific Version

```bash
$ git reset --hard commit_id
```

`commit_id` is the version number, a sequence calculated by SHA1.

### Discard Changes in the Staging Area

1. Discard changes and return to the working directory.

```bash
$ git reset HEAD <file>
```

2. Undo modifications in the working directory.

```bash
$ git checkout -- <file>
```

Tips:
1. If you mess up the content of a file in the working directory and want to discard the changes, use the command `git checkout -- <file>`.
2. If you not only mess up the content of a file in the working directory but also add it to the staging area, and want to discard the changes, follow these two steps: first use `git reset HEAD <file>` to return to step one, then use the command from step one.
3. If you have already committed inappropriate changes to the version repository and want to undo the commit and revert to a previous version, provided you have not pushed to the remote repository.

### Important Note about `git checkout`
The `--` in the `git checkout -- file` command is **very important!** Without `--`, it becomes a command to **switch to another branch**.