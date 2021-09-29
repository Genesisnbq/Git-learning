<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-29 16:20:21
 * @LastEditTime: 2021-09-29 16:20:22
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/ 17_怎样把连续的多个commit整理成1个.md
-->

# 17 | 怎样把连续的多个commit整理成1个？

>git rebase -i 开始commit [结束commit], 在执行这个命令时，
>如果没有指定 结束commit,那么结束commit 默认为当前分支最新的 commit，那么rebase 结束后会自动更新当前分支指向的 commit,
>如果指定了结束 commit，而且结束 commit不是当前分支最新的 commit，那么rebase 后会有生成一个 游离的 head,，而且当前分支指向的commit 不会更新

```
git log --graph # 美化git log

```

![3.jpg](https://i.loli.net/2021/09/29/K2PBy9H7C6VhXWr.jpg)

## 1. 合并多个commit

```sh
# 选择最下面的这个commit（父
git rebase -i 9c6861

```

![2.jpg](https://i.loli.net/2021/09/29/FrvOUTXsJ51klIC.jpg)

将 41， 27， 8f这三个commit 合并到 9c中去

## 2. 增加合并原因

![4.jpg](https://i.loli.net/2021/09/29/oIQCVrSHBpM576W.jpg)



## 3. 自己的总结

1. `git log --oneline`

![2.jpg](https://i.loli.net/2021/09/29/365HsWXNj7CIaoY.jpg)

2. 在上面的是比较古老的commit， 因此将下面每个pick改为s， 即可融合（meld）
3. 最后给这一次变更填写一个理由（Create a combination of 4 commits.

