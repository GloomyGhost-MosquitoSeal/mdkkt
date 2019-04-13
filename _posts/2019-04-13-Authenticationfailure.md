---
layout: solution
title: "Authentication failure"
description: "Linux su 命令授权错误"
category: "Linux Bash"
date: "2019-04-13"
---

# 错误内容示例：

## 示例1:

```bash
linux@linux: ~$ su
Password:
su: Authentication failure
```

## 示例2:
```bash
linux@linux: ~$ su
密码:
su：鉴定故障
```

# 详细解析：
Linux 的 root 用户一般在配置的时候是没有密码的，必须设置才可以使用

# 解决方法

## 方法一：
使用`sudo -i`代替`su`命令

```bash
linux@linux: ~$ sudo -i
```

## 方法二：
设置root密码

```bash
linux@linux: ~$ sudo passwd root
```

## 方法三：
直接进入root，免去授权

```bash
linux@linux: ~$ sudo su
```