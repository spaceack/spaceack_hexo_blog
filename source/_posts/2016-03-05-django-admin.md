---
title: Django admin 扩展
date: 2016-03-05 12:00:00
categories: Python
tags: 
  - Django
---

## 后台管理改为中文

```python
#  将 setting.py  配置选项设置为中文
LANGUAGE_CODE = 'en-us'
TIME_ZONE = 'UTC'

LANGUAGE_CODE = 'zh-Hans'
TIME_ZONE = 'Asia/Shanghai'
```

![更改前]()

![更改后]()



## 后台标题和名称的修改（title/header）

```python 
# admin.py 文件添加 修改网页title和站点header
admin.site.site_header = 'XXX平台-管理系统'
admin.site.site_title = 'XXX平台'
```

## 创建Admin 超级管理员账号
```bash
python manage.py createsuperuser
```


## 将数据表添加到站点管理

1. 在`settings.py`文件,`INSTALLED_APPS` 加入该app.
2.  在该app目录的`admin.py`文件下注册
```python
from django.contrib import admin
from .models import Baseipweb
class BaseipWebAdmin(admin.ModelAdmin):
    pass

admin.site.register(Baseipweb, BaseipWebAdmin)
```

## 数据记录对象以字段显示


## 图像预览显示
