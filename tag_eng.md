## Tags
A tag is a meaningful and easy-to-remember name associated with a specific commit.

### Create a New Tag

```bash
$ git tag <tagname>
```

The command `git tag <tagname>` creates a new tag, which by default points to the HEAD commit. You can also specify a commit ID.

### Specify Tag Information

You can specify tag information using the following format: `git tag -a <tagname> -m "say something..."`

```bash
$ git tag -a <tagname> -m <description> <branchname> or commit_id
```

### PGP-Signing Tags

You can sign tags with PGP using the following format: `git tag -s <tagname> -m "say something..."`

```bash
$ git tag -s <tagname> -m <description> <branchname> or commit_id
```

### View All Tags

```bash
$ git tag
```

### Push a Local Tag

```bash
$ git push origin <tagname>
```

### Push All Local Tags That Have Not Been Pushed Yet

```bash
$ git push origin --tags
```

### Delete a Local Tag

```bash
$ git tag -d <tagname>
```

### Delete a Remote Tag

```bash
$ git push origin :refs/tags/<tagname>
```