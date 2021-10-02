<!--
 * @Author: Binqi Ni
 * @Date: 2021-10-02 07:56:17
 * @LastEditTime: 2021-10-02 07:56:17
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/03_Git与GitHub的简单同步 (4讲)/33_把本地仓库同步到Github.md
-->
# 33_把本地仓库同步到Github
> 个人笔记总结
git remote -v 查看远程版本库信息
git remote add githup <url> 添加githup远程版本库
git fetch githup 拉取远程版本库
git merge -h 查看合并帮助信息
git merge --allow-unrelated-histories githup/master 合并githup上的master分支（两分支不是父子关系，所以合并需要添加 --allow-unrelated-histories）
git push githup 推送同步到githup仓库



## 补充

lvanyu:

老师，我们的工作场景比较特殊，有一个甲方和乙方共研项目。2个gitlab，其中甲方有内外网物理隔离，也就是说2个gitlab没法联网。
目前采用git clone --bare {url}加U盘拷贝杀毒进入内网，再使用git push --mirror {url}方式全量同步到甲方gitlab。计划2周同步一次。
这种方式存在共研后期分支代码合并问题，如何处理？
请问是否有更好的解决方案。

> 作者回复: 我们的做法是：为对外合作项目单独搭建了一个gitlab，公司内部员工用内网域名，合作方用外网域名，并且为外网IP设置了白名单，只有授权的IP才能访问公司的gitlab

