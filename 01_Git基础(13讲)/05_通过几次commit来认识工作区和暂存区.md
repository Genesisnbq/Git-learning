<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-18 01:17:37
 * @LastEditTime: 2021-09-18 01:17:38
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/05_通过几次commit来认识工作区和暂存区.md
-->

# 05 | 通过几次commit来认识工作区和暂存区

## 1. 往仓库里添加文件

<img src="https://i.loli.net/2021/09/18/68ozp2rd9nHVLiQ.jpg" alt="6.jpg" style="zoom:50%;" />

`git status`: 经常用到这个命令查看git 与 当前仓库 和 暂存区的关系

`git add`: 将未被git管理的文件加入暂存区（被管理

`git commit -m "xxxx"`: 上一次变更修改了什么



## 2. 如何修改未提交的commit

`git rebase -i HEAD~n`: n为倒数n条

​	进入插入模式， 将pick 改为 edit

`git commit --amend` : 修改上次的commit

`git rebase --continue`: 修改commit

