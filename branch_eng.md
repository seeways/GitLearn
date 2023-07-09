## Branching

### Common Branching Commands

```bash
View branches: git branch

Create a branch: git branch <name>

Switch to a branch: git checkout <name>

Create and switch to a branch: git checkout -b <name>

Merge a branch into the current branch: git merge <name>

Delete a branch: git branch -d <name>
```

### Branching Strategy

In actual development, we should follow several basic principles for branch management:

1. The master branch should be very stable and used only for releasing new versions. It should not be used for regular work.

2. Development should be done on the dev branch, which means the dev branch is unstable. When a version is ready for release, it should be merged into the master branch for the release.

3. You and your teammates should work on the dev branch, each having your own branch. Periodically, merge your changes into the dev branch.

4. If there are intermediate versions like test versions or pre-release versions, follow the priority and process to merge them recursively from dev to master.

5. When merging branches, use the `--no-ff` parameter to perform a regular merge. This preserves the branch history, indicating that a merge was performed. In contrast, fast-forward merges do not show the merge history.

### Create a Branch

```bash
$ git branch <branchname>
```

### View Local Branches

Show all branches.

```bash
$ git branch
```

### View Remote Branches

'r' for remote.

```bash
$ git branch -r
```

### View All Branches

'a' for all.

```bash
$ git branch -a
```

### Switch Branch

```bash
$ git checkout <branchname>
```

### Create and Switch to a Branch
```bash
$ git checkout -b <branchname>
```

### Merge a Branch into the Current Branch

```bash
$ git merge <branchname>
```

### Delete a Branch

```bash
$ git branch -d <branchname>
```

### Force Delete

```bash
$ git branch -D <branchname>
```

### View Branching Graph

**When Git cannot automatically merge branches, conflicts must be resolved first.** After resolving conflicts, you can continue with the operation.

```bash
$ git log --graph
```

### View Branch Tree (Compact Version)

Why type such a long command? Because the tree can be long, and the compact version allows you to see the architecture at a glance.

```bash
git log --graph --pretty=oneline --abbrev-commit
```

### Regular Merge Mode: Disable `--no-ff`

Since this merge creates a new commit, use the `-m` parameter to add a commit message.  

By using the `--no-ff` parameter when merging branches, a regular merge is performed. This shows that a merge was performed, including author and timestamp information. In contrast, fast-forward merges do not show the merge history.

```bash
$ git merge --no-ff -m "description" <branchname>
```



### Save the Work in Progress

```bash
$ git stash
```

### View Stash List

```bash
$ git stash list
```

### Restore the Work in Progress

However, after restoration, the stash content is not deleted. You need to manually delete it.

```bash
git stash apply
```

### Delete the Work in Progress

```bash
git stash drop
```

### Automatically Delete the Work in Progress After Restoration

```bash
git stash pop
```

### Restore a Specific Work in Progress

```bash
git stash apply <stash version>
```

### Discard an Unmerged Branch

```bash
$ git branch -D <branchname>
```

### View Remote Repository Information

```bash
$ git remote -v
```

### Create a Local Branch Corresponding to a Remote Branch

It is recommended to keep the names of local and remote branches the same.

```bash
$ git checkout -b branch-name origin/branch-name
```

### Establish an Association between Local and Remote Branches

```bash
$ git branch --set-upstream branch-name origin/branch-name


Set branch-name to track the remote branch origin/branch-name.
Use --track or --set-upstream-to to establish the association.

$ git branch --track branch-name origin/branch-name;
```

### Push a Branch from Local to Remote

If the push fails, use `git pull` to fetch new commits from the remote first.

```bash
$ git push origin branch-name
```


### Fetch a Branch from Remote

If there are conflicts, resolve them first.

```bash
$ git pull
```