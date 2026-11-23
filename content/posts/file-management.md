---
title: "Linux 文件管理与权限"
date: 2026-11-22
draft: false
categories: ["实验报告"]
tags: ["文件权限", "chmod"]
---

## 文件权限管理
Linux 中使用 `ls -l` 可以查看文件属性。权限分为读(r)、写(w)、执行(x)。

使用 `chmod u+x a.txt` 可以给属主添加执行权限。
使用 `chmod u-r a.txt` 可以去掉属主的读权限。
