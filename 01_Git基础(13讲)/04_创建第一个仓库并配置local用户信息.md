<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-18 00:38:52
 * @LastEditTime: 2021-09-18 00:38:52
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/04_创建第一个仓库并配置local用户信息.md
-->

# 04 | 创建第一个仓库并配置local用户信息

## 建Git仓库

两种场景：

1. 把已有的项目代码纳入Git管理

   ```sh
   cd 项目代码所在的文件夹
   git init
   
   ```

2. 新建的项目直接用Git管理

   ```shell
   cd 某个文件夹
   git init your_project #会在当前路径下创建和项目名称同名的文件夹
   cd your_project
   ```

`git add 文件名`：将此文件添加到暂存区

`git commit -m'xxxx'`: 填写此次变更的理由

`git status`: 查看git现在的状况

`git log`: 查看git的日志
