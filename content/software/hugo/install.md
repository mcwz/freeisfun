---
title: 安装 Hugo
weight: 10
---

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