---
title: Linux 常用命令
date: 2014-09-10 12:00:00
categories: Linux
tags: 
  - Linux
  - tools
  - 配置 
---

##  系统篇
### CPU
```bash
lscpu
cat /proc/cpuinfo

```
### 内存

```bash 
# 查看主板内存插槽数及使用情况
dmidecode|grep -P -A 5 "Memory\s+Device" | grep Size|grep -v Range

# 查看主板支持最大内存
sudo dmidecode | grep -P 'Maximum\s+Capacity'

# 查看内存频率
sudo dmidecode | grep -A16 "Memory Device"|grep 'Speed'

# 查看内存及交换空间使用情况
# -h 以 Gibibytes为单位查看.
free -m

```
### 硬件设备
```bash
# 查看硬件设备
lshw

```


## 传输篇 scp
```bash
# 使用scp 传输文件 将本地文件data.zip 传到服务器 /data 目录 -
# P ssh端口号
scp -P 22 /data/data.zip root@spaceack.com:/data

# 使用scp 传输文件 将远程目录 remote_path 传到本地当前目录
scp   remote_username@remote_ip:/remote_path/*  .
```
## 其它
```bash
# 查看主机 ssh 连接数
w | grep pts |wc -l

# 文件批量重命名
apt install rename 
```
### 选择时区 tzselect
```bash
tzselect
# 查看时间
date
```