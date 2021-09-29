<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-29 15:28:43
 * @LastEditTime: 2021-09-29 15:28:43
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/16_怎么修改老旧commit的message.md
-->

# 16 | 怎么修改老旧commit的message？

`git rebase -i xxxx`： xxxx指的是要被修改的commit的父亲

> **尚未提交到远端服务器的commit，是可以rebase的。**
>
> rebase 团队开发一般情况下， 不允许使用

对基（base）进行变更：
      在变基的时候，因为新的base的commit没有基于任何一个分支，所以处于分离头指针状态，git接下来会在我们修改message那个commit往后依次对后面的commit修改hash值但不更改commit的文件内容,让后续的commit的hash值都是基于修改mseeage之前的那个commit依次更新！



`git rebase -i --root` : 修改root的commit 



## 不推荐使用 rebase

>    对于团队中公用的分支，例如发布分支等，禁用 rebase，因为这样会破坏历史的 commit 信息的，将来要溯源、基于构建历史拉取补丁分支等就会带来极大不便

