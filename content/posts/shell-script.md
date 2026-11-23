---
title: "Shell 脚本编程：one2n 求和脚本"
date: 2026-11-22
draft: false
categories: ["Linux课程"]
tags: ["Shell", "脚本"]
---

## 编写 one2n 脚本
本实验要求编写一个从 1 加到 n 的 Shell 脚本。

```bash
#!/bin/bash
if [ $# -ne 1 ]; then
    echo "用法: $0 n"
    exit 1
fi
n=$1
sum=0
for ((i=1; i<=n; i++)); do
    sum=$((sum+i))
done
echo "结果: $sum"
