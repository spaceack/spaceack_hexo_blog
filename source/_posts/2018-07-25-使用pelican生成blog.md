---
title: 使用pelican生成blog
date: 2018-07-25 12:00:00
update: 2018-07-25 12:00:00
author: 小云吞
categories: Blog
tags: 
  - pelican
---

###  md/rst 文件生成 html 到 output目录 
```pelican content -o spaceack.github.io```

### 客本地预览, 开启本地简易web服务
默认端口: 8000, 有autoload特性

```cd output && python3 -m pelican.server```

