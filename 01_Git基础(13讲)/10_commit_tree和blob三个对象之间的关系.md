<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-23 09:55:56
 * @LastEditTime: 2021-09-23 10:39:45
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/01_Git基础(13讲)/10_commit_tree和blob三个对象之间的关系.md
-->

# 10 | commit、tree和blob三个对象之间的关系

>git有3种对象：commit、tree、blob。每次的提交，都是一个commit，一个commit又是包含了一棵tree，每个tree里面又是包含了多棵tree和blob，而文件的的最终形式是erwtoyoipu blob。对于blob，git会认为文件内容相同，就使用同一个blob，这样就极大的避免了频繁的提交时，git的存储空间的急剧上升。
>
>

![1.jpg](https://i.loli.net/2021/09/23/PGmrQ7l3naUXVwH.jpg)

  

## 常用命令

`git cat-file -p 哈希值` 查看文件内容

blob中的内容是可见的















