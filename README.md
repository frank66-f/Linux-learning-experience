# 基于 Hugo + PaperMod 搭建个人博客

## 项目简介
本项目基于 Linux 虚拟机环境，使用 Hugo 静态网站生成器和 PaperMod 主题搭建个人博客。
包含功能：首页个人简介、关于页面（含照片）、标签、分类、归档、本地搜索。

## 访问方式
- **方式 A（本地虚拟机访问）**：在虚拟机运行 `hugo server --bind 0.0.0.0 -D`，宿主机通过 `http://localhost:1313/Linux-learning-experience/` 访问。
- **方式 B（GitHub Pages 外网访问）**：https://frank66-f.github.io/Linux-learning-experience/

## 遇到的主要问题及解决办法
1. **Hugo 主题不兼容（GLIBC 报错）**：Ubuntu 20.04 系统自带的 GLIBC 库版本较低，无法运行最新版 Hugo。通过下载兼容的 Hugo `v0.128.2 extended` 版本，并搭配旧版 PaperMod `v7.0` 主题解决。
2. **网络连接失败（GnuTLS error）**：使用 HTTPS 推送到 GitHub 时因网络环境报错。通过生成 SSH Key 并添加到 GitHub 账号，将远程仓库地址改为 SSH 协议成功推送。
3. **Actions 自动构建失败**：云端默认使用了最新版 Hugo，导致主题模板解析报错。通过在 `.github/workflows/hugo.yaml` 中指定 `hugo-version: '0.128.2'` 解决。
