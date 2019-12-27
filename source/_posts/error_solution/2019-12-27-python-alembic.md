---
title: ERROR [root] Error: Can't locate revision identified by '' Solution 
date: 2019-12-27 12:00:00
categories: ErrorSolution
tags: 
  - alembic 
---

 - 出错信息：

```bash
$ python mange.py db migrate

INFO  [alembic.runtime.migration] Context impl MySQLImpl.
INFO  [alembic.runtime.migration] Will assume non-transactional DDL.
ERROR [root] Error: Can't locate revision identified by 'e884a332f0f7'
```
- 解决：

alembic_version 版本号与 迁移号不一致，需要清除旧数据。

```sql
truncate table alembic_version;
```