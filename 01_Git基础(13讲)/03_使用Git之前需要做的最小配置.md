<!--
 * @Author: Binqi Ni
 * @Date: 2021-09-18 00:27:33
 * @LastEditTime: 2021-09-18 00:27:34
 * @LastEditors: Binqi Ni
 * @FilePath: /Git-learning/01_Git基础(13讲)/03_使用Git之前需要做的最小配置.md
-->

# 03 使用Git之前需要做的最小配置

## 1. 配置User信息

> 配置 user.name 和 user.email

```shell
git config --global user.name 'your_name'
git config --global user.email 'your_email@domain.com'
```

## 2. config的三个作用域

**缺省等同于local**

```shell
git config --local #local只对某个仓库有效
git config --global #global对当前用户所有仓库有效
git config --system #system对系统所有登录的用户有效
```

**显示config 的配置， 加 --list**

```shell
git config --list --local
git config --list --global
git config --list --system
```

