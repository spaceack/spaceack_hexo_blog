---
title: Linux 常用环境变量
date: 2017-06-19 12:00:00
categories: Linux
tags: 
  - Linux
  - 配置 
---

```bash
# jdk env
JAVA_HOME=/opt/jdk
CLASSPATH=.:$JAVA_HOME/lib.tools.jar
PATH=$JAVA_HOME/bin:$PATH
export JAVA_HOME CLASSPATH PATH

# go env
GOROOT=/opt/go
GOPATH=$HOME/go
PATH=$PATH:$GOROOT/bin

# redis env
export PATH=$PATH:/opt/redis/bin 

# node.js env
export PATH=$PATH:/opt/node/bin

alias datagrip='/opt/datagrip/bin/datagrip.sh'
alias pycham='/opt/pycharm/bin/pycharm.sh'

```