<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-23 15:43:15
 * @LastEditTime: 2021-09-23 21:48:52
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/01_Git基础(13讲)/11_小练习_数一数tree的个数.md
-->

# 11 | 小练习：数一数tree的个数

>`git add` 之后， git会自动在暂存区创建一个blob对象
>
>`git commit`之后， git会自动创建一个commit对象
>
>

![1.jpg](https://i.loli.net/2021/09/23/r6EBfTqyFe7h5k2.jpg)

Q&A

>1. 最后那个小练习，为什么中间需要有2个tree，一个tree不可以吗？多个tree的原因是什么？
>
>   作者回复: 让blob成为基础组件，可以利用树把多个文件特定版本对应的blob进行灵活的组装。
>
>   blob（代表文件的内容）可以充分地被复用。
>
>2. 


