<!--
 * @Author: Binqi Ni
 * @Date: 2021-10-01 16:50:58
 * @LastEditTime: 2021-10-01 17:05:42
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/28_如何指定不需要Git管理的文件.md
-->

# 28 | 如何指定不需要Git管理的文件？

> 通过.gitignore设置git不用管理文件或文件夹



太阳鸟：

如果提交commit后，想再忽略一些已经提交的文件，怎么处理？

answer： The problem is that .gitignore ignores just files that weren't tracked before (by git add). Run git reset name_of_file to unstage the file and keep it. In case you want to also remove given file from the repository (after pushing), use git rm --cached name_of_file.

把想忽略的文件添加到 .gitignore ；然后通过 git rm --cached name_of_file 的方式删除掉git仓库里面无需跟踪的文件。



五月：

如果是文件夹就是
filename/

如果是某个具体的文件就是
filename.后置名

如果是某个结尾的文件
*.后置名
