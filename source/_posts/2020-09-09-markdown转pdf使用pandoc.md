---
title: markdown转pdf使用pandoc
author: 小云吞
date: 2020-09-09 21:00:00
update: 2020-09-09 21:00:00
categories: tools
tags: 
  - tools
  - pandoc
---

- step1: 安装pandoc
```bash
sudo apt install pandoc
```
- step2: 安装转换pdf引擎 wkhtmltopdf
[下载地址](https://wkhtmltopdf.org/downloads.html)

- step3: 执行转换
```bash
pandoc --pdf-engine=wkhtmltopdf --metadata pagetitle="Spaceack的算法笔记"  算法笔记.md -o 算法笔记.pdf
```
## 示例：

![pdf效果](notebookpdf.png)

```markdown
    # 算法笔记
    ## 线性表

    python的`list`是可变线性表。

    1. len()是 O（1）操作
    2. 元素访问和赋值，尾端加入和尾端删除（包括尾端切片删除）都是O（1）操作。
    3. 一般位置的元素加入，切片替换，切片删除，表拼接（extend）都是O（n）操作。
    4. pop操作默认为删除表尾元素并将其返回O（1），指定非尾端位置为O（n）时间复杂度。

    5. `lst.clear()`清除表lst所有元素O（1）操作。两种实现方式：
    a. 元素记数值（表长度）设置为0。实现简单，操作效率高，但不能真正释放占用的存储。若表很长，执行操作后表内没有元素，但仍会占用原有大块内存。

    b. 另分配一个空表用的存储区，原存储区直接丢弃。若表又一次增大，会频繁更换存储区。

    6. `lst.reverse()`修改表lst自身，元素顺序倒置O（n）
        
        ```python
        def reverse(self):
            elems = self.elements
            i, j = 0, len(elems) - 1
            while i < j：
                elems[i], elems[j] = elems[j], elems[i]
                i, j = i+1, j-1
        ```

    ## 链接表
    ### 条件
    1. 能够找到表中的首元素。
    2. 从任一元素出发，可以找到下一个元素。

    ### 单链表

    - 定义

    ```python
    class LNode:
        def __init__(self, elem, next_= None):
            self.elem = elem
            self.next = next_
    ```

    ## 树

```

