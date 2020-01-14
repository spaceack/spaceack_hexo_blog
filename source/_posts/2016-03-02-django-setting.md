---
title: Django setting.py 模板
date: 2016-03-02 12:00:00
categories: Python
tags: 
  - Django
  - 配置
---

## DATABASES 模板
```python
## DATABASES

### sqlite3
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}

### mysql
DATABASES = { 
    'default': { 
        'ENGINE': 'django.db.backends.mysql', 
        'NAME': 'mydb', #数据库名称(需要先创建) 
        'USER': 'root', # 数据库用户名 
        'PASSWORD': '123456', # 数据库密码 
        'HOST': '', # 数据库主机，留空默认为localhost 
        'PORT': '3306', # 数据库端口 
        } 
    }

### Postgresql

DATABASES = { 
    'default': { 
        'ENGINE': 'django.db.backends.postgresql_psycopg2', 
        'NAME': 'mydb', # 数据库名字(需要先创建) 
        'USER': 'postgres', # 登录用户名 
        'PASSWORD': '123456', # 密码 
        'HOST': '', # 数据库IP地址,留空默认为localhost 
        'PORT': '5432', # 端口 
        } 
    }
    
```

## Internationalization 模板
``` python
LANGUAGE_CODE = 'zh-Hans'
TIME_ZONE = 'Asia/Shanghai'
```
