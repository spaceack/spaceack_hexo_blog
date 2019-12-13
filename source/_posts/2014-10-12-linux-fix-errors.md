---
title: Linux 错误修复笔记
date: 2014-10-12 12:00:00
categories: Linux
tags: 
  - Linux
---

## apt

- 错误 ："subprocess installed post-installation script returned error exit status 1"
- 故障排除：

```bash

apt-get autoclean
apt-get autoremove
apt-get update
apt-get upgrade
```