<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-29 17:00:21
 * @LastEditTime: 2021-09-29 17:00:21
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/18_怎样把间隔的几个commit整理成一个.md
-->



# 18_怎样把间隔的几个commit整理成一个.md

## 1. 实战演练

1. 

![1.jpg](https://i.loli.net/2021/09/29/C3k7hAdHpn9uPeQ.jpg)

>由于 readme没有parent， 因此先填readme的 commit
>
>`git rebase -i f09122cf21f`

2.

![2.jpg](https://i.loli.net/2021/09/29/V3Qvpf1tKeJ5EYS.jpg)

>只会出现两个， 这是不够的
>
>我们需要将最古老的写在最上面
>
>1. 在最上面加上 `pick f09122c` 
>2. 将 5cc5aa3 放到 34e735d上面， 并写上 `s 5cc5aa3 Move filename readme to readme.md`
>3. 将原本的5cc5aa3 删除

## 2. rebase之后， 如何复原

1. git reflog 找到rebase下面的 哈希值
2. git reset --hard <找到的哈希值> 即可
