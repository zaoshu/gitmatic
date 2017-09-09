# Git Commit Message 模版

[English](./README.md)

所有模版均基于由 [Deekshith Allamaneni](https://github.com/adeekshith) 创建的[模版](https://gist.github.com/adeekshith/cd4c95a064977cdc6c50).

## 设置方法 

使用以下 git 命令来设置 commit message 模版:

```bash
# 全局设定 
$ git config --global commit.template <.git-commit-template.txt file path> 
# 本地仓库设置 
$ git config commit.template <.git-commit-template.txt file path> 
```

你也可以通过直接修改 git 配置来实现:

1. 使用 VIM 打开 git 配置文件:

```bash
$ vim <your-repo-path>/.git/config 
# 全局配置文件: ~/.gitconfig
```

2. 编辑 `template` 区域下 `commit` 的值:（如果没有该区域请自行创建）

```bash
[commit]
    template = /usr/local/etc/gitmatic/templates/gitmessage-zh
```

3. 回到你的代码仓库通过 `git commit -a` 提交 commit，你便可以看到新的模版已经生效:

```bash
# <类型>: <内容概述> 
# |<-----  请保持单行简介长度不超过此行长度  ----->|

# <详情>
# |<----------------  请保持每行内容长度不超过该行长度  ---------------->|


# <引用来源> <引用内容>


# --- COMMIT END ---
# 类型枚举：
#    feat     (新功能)
#    fix      (问题修复)
#    refactor (代码重构)
#    style    (代码风格改动、格式变化等，无实现改动)
#    docs     (文档更新)
#    test     (增加、重构测试，无实现改动)
#    chore    (修改一些配置文件如 .gitignore 等，无实现改动)

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

## 模版命名约定 

模版名称由以下部分组成

```
gitmessage-${语言}[-full]
```

以 `-full` 结尾的模版包含了 message 组成区域的解释以及书写的指导，推荐新手选择该模版上手，在熟悉书写规范后换成简单版本。



