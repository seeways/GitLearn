### View Logs

```bash
$ git log
```

### Simplified Log

```bash
$ git log --pretty=oneline
```

### View the Last N Commits

```bash
git log -n
```

### Change Log

`-n` as above; if not specified, it displays all.

```bash
git log --stat -n
```

### View Commit Changes

View the modifications made in a specific commit.

```bash
git show <commit-hash-id>
```

### Exit Log Status

Sometimes, when the log is too long, you can press "q" in the terminal to exit the log view.

### View HEAD History and Descriptions

```bash
$ git reflog
```