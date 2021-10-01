<!--
 * @Author: Binqi Ni
 * @Date: 2021-10-01 17:25:00
 * @LastEditTime: 2021-10-01 17:25:01
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/29_如何将git仓库备份到本地.md
-->

#  29 | 如何将Git仓库备份到本地？

## 1. 常用的传输协议

![1.jpg](https://i.loli.net/2021/10/01/4ItvOV7KFThARDe.jpg)

## 2. 哑协议与智能协议的区别

直观区别：哑协议传输进度不可见；只能协议传输可见

传输速度：智能协议比哑协议传输速度快



## 3. 备份特点

![2.jpg](https://i.loli.net/2021/10/01/KmlCS2TXujRwHIk.jpg)





## 4. 操作

`git clone --bare /Users/nibinqi/Coding/Git-learning/.git ya.git` : 哑协议克隆一个裸仓库

`git clone --bare file:///Users/nibinqi/Coding/Git-learning/.git zhineng.git` : 智能协议克隆一个裸仓库



1. 通过智能协议本地备份

   `git remote -v` : 查看现有的remote

   如果没有： `git remote add <remote-name> file:///Users/nibinqi/Coding/Git_backup/zhineng.git`

2. 通过`git branch -v` : 查看当前仓库有多少个分支

3. 通过`git push zhineng` : 进行推送



## 5. 补充

Lighting:

\# 本地模拟推送，git备份

\## 远程库

git clone --bare file:///XXXX/.git remoteRepoName.git

bare不包含工作区，作为远端，以后备份方便一点

这样的话，已经备份了

\## 本地仓库

跟远程库建立关联

git remote add remoteRepoName file:///XXXX/remoteRepoName.git

本地发送一些改动，比如新增分支develop

推送分支变动到远程

git push --set-upstream remoteRepoName develop

再到远程库下面查看就会发现远程也有develop分支了



