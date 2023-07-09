### Common Ignore Files

You can find a list of common ignore files at this link: [https://github.com/seeways/MyIgnore](https://github.com/seeways/MyIgnore)

### Configure Aliases

```bash
git config --global alias.<name> <git-name>
```

It is recommended to use aliases after becoming familiar with Git commands.

```bash
# Set an alias
git config --global alias.unstage 'reset HEAD'

# Use the alias to unstage changes (Equivalent to git reset HEAD test.py)
git unstage test.py
```

Aliases are especially useful for long commands. For example:

```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

This creates an alias `lg` for a prettier log output. You can use it like `git lg`.

### Display Colors

If the changes in files are not displayed in color by default, it is recommended to enable this option.

```bash
git config --global color.ui true
```

### git config

1. When configuring Git, using the `--global` option applies the configuration to the current user. If not used, it only applies to the current repository.
2. The Git configuration for a repository is stored in the `.git/config` file of that repository.
3. The global Git configuration file is located in the user's home directory and named `.gitconfig` (a hidden file).
4. If you want to modify or remove a configuration or alias, you can directly edit or delete the respective configuration file.