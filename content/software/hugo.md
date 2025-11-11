---
title: "Hugo 开源软件介绍｜安装、使用与避坑指南"
date: 2025-06-25
# 静态字段：不变或半年才变一次
repo: "https://github.com/gohugoio/hugo"
license: "Apache-2.0"
language: "Go"
slogan: "世界上最快的静态网站生成器"
platforms: ["🪟 Windows", "🍎 macOS", "🐧 Linux"]
tags: ["静态网站生成器", "Go", "博客", "文档站"]
#  semi-static：每天自动抓一次（可选）
stars: 74000
last_commit: "2025-06-24"
binary_size: "≈ 20 MB"
---

## 基本简介
Hugo 是用 **Go** 写的超高速静态网站生成器：无需数据库、一条命令就能把 Markdown 变成完整网站，适合个人博客、产品文档、公司官网。

## 使用场景
| 场景 | 示例 | 一句话效果 |
|---|---|---|
| 快速开个人博客 | `hugo new site myblog` | 3 分钟搭好，自动热重载，写完即发布。 |
| 给开源项目写文档 | 官方主题 Docsy | 自动生成侧边栏、搜索、多语言，免配置。 |
| 公司官网落地页 | 原生 + 任意主题 | 一键导出静态 HTML，直接丢 CDN，省钱又安全。

## 硬核指标
- **语言**：Go 1.22，编译后单文件
- **速度**：~1 ms/页，1 万页 &lt; 2 秒（M2 实测）
- **主题**：官方库 300+，Star 前十均支持暗黑/搜索/多语言
- **热重载**：保存即刷新，浏览器 WebSocket 实时同步
- **输出**：HTML、AMP、JSON、RSS、Sitemap 自动生成

## 系统要求
| 系统 | 最低版本 | 内存 | 磁盘 | 备注 |
|---|---|---|---|---|
| Windows | 10 1903 | 512 MB | 100 MB | 无需 Go 环境 |
| macOS | 11 Big Sur | 512 MB | 100 MB | Apple / Intel 双架构 |
| Linux | 内核 3.10 | 512 MB | 100 MB | glibc ≥ 2.17 |

## 安装路径
### 小白 3 步
1. 根据系统自动下载：
   - [Windows exe](https://github.com/gohugoio/hugo/releases/download/v0.135.0/hugo_0.135.0_windows-amd64.zip)
   - [macOS dmg](https://github.com/gohugoio/hugo/releases/download/v0.135.0/hugo_0.135.0_darwin-universal.tar.gz)
2. 解压后把 `hugo`（或 `hugo.exe`）拖到任意目录 → 双击即装。
3. 打开终端/命令行，输入  
   `hugo version` 出现版本号 = 成功。

### 老司机 1 行
```bash
# macOS brew
brew install hugo

# Windows winget
winget install Hugo.Hugo.Extended

# Arch
sudo pacman -S hugo

# Docker（不装也能跑）
docker run --rm -v $(pwd):/src klakegg/hugo:0.135.0 server -p 8080