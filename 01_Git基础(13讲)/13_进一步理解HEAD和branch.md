<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-27 23:49:25
 * @LastEditTime: 2021-09-27 23:49:25
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/01_Git基础(13讲)/13_进一步理解HEAD和branch.md
-->

# 13 | 进一步理解HEAD和branch

`git checkout -b <new-branch-name> [master/其他分支/commit]`: 创建新分支， 并且直接切换到这个分支上

`git diff xxx xxx` : 比较差异

​	`git diff HEAD HEAD^1` : 比较HEAD 与 HEAD父亲之间的比对

​	`git diff HEAD HEAD^1^1`:          HEAD父亲的父亲



## 补充

开始讲HEAD的使用，以及PARENT符号^和~。我觉得这里几个地方没讲清楚
1 一个节点，可以包含多个子节点（checkout 出多个分支）
2 一个节点可以有多个父节点（多个分支合并）
3 \^是~都是父节点，区别是跟随数字时候，^2 是第二个父节点，而~2是父节点的父节点
4 ^和~可以组合使用,例如 HEAD~2^2

