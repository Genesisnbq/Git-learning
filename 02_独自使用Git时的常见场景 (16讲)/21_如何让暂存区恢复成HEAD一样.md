<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-30 17:04:02
 * @LastEditTime: 2021-09-30 17:04:02
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/02_独自使用Git时的常见场景 (16讲)/21_如何让暂存区恢复成HEAD一样.md
-->

# 如何让暂存区恢复成HEAD一样

`git reset HEAD` ： 恢复暂存区与HEAD一致

> reset命令不加 --hard，则暂存区的内容恢复成HEAD对应的内容，工作区的变更继续保留。
>
> 如果加了 --hard，则不管工作区还是暂存区，内容都变回HEAD对应的内容。

`git reset HEAD` 将暂存区的恢复成HEAD 一样，暂存区的内容会回退到工作区。
`git reset HEAD` filename， 只是将暂存区指定文件的恢复成HEAD .
`git diff --cached` 比对暂存区与HEAD 差别。

