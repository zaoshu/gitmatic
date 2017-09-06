# Git Commit Message Templates

[中文](./README-ZH.md)

All the templates are based on this [gist](https://gist.github.com/adeekshith/cd4c95a064977cdc6c50) created by [Deekshith Allamaneni](https://github.com/adeekshith).

## Setup 

Change the commit message template by:

```bash
# global setting
$ git config --global commit.template <.git-commit-template.txt file path> 
# or local setting
$ git config commit.template <.git-commit-template.txt file path> 
```

Or you can edit your git config file directly:

1. Open your git config file by VIM: 

```bash
$ vim <your-repo-path>/.git/config 
# global config path: ~/.gitconfig
```

2. Modify the var `template` under section `[commit]`: (create one if there's none)

```bash
[commit]
    template = /usr/local/etc/gitmatic/templates/gitmessage-zh
```

3. Head back to your repository and type  `git commit -a`, and you shall see the new templates:

```bash
# <type>: <subject> (Max 50 char)
# |<----  Using a Maximum Of 50 Characters  ---->|

# <context>
# |<----   Try To Limit Each Line to a Maximum Of 72 Characters   ---->|


# <reference source> <reference content>


# --- COMMIT END ---
# Type can be 
#    feat     (new feature)
#    fix      (bug fix)
#    refactor (refactoring production code)
#    style    (formatting, missing semi colons, etc; no code change)
#    docs     (changes to documentation)
#    test     (adding or refactoring tests; no production code change)
#    chore    (updating grunt tasks etc; no production code change)

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch feature/templates-readme
# Changes to be committed:
#       new file:   templates/README.md
#
# ------------------------ >8 ------------------------
# Do not touch the line above.
# Everything below will be removed.
diff --git a/templates/README.md b/templates/README.md
new file mode 100644
index 0000000..d35b72c
--- /dev/null
+++ b/templates/README.md
@@ -0,0 +1,55 @@
+# Git Commit Message Templates

...
```

## Templates Name Convention

The name of template is composed as:

```
gitmessage-${LANG}[-full]
```

Template with `-full` suffix contain section explaination and writing instruction. For beginners, I recommmand you to use the `-full` version to get it started, and you can switch to the short version in future when you're familiar with all the stuff.



