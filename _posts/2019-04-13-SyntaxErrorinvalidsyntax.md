---
layout: solution
title: SyntaxError: invalid syntax
description: 语法错误
category: Python
date: 2019-04-13
---

# 错误内容示例：

```Python
>>> while True print('Hello world')
  File "<stdin>", line 1
    while True print('Hello world')
                   ^
SyntaxError: invalid syntax
```

# 详细解析：
解析器会输出出现语法错误的那一行，并显示一个“箭头”，指向这行里面检测到第一个错误。 错误是由箭头指示的位置 上面 的 `token` 引起的（或者至少是在这里被检测出的）：在示例中，在 print() 这个函数中检测到了错误，因为在它前面少了个冒号 (':') 。文件名和行号也会被输出，以便输入来自脚本文件时你能知道去哪检查。

# 正确实例：

```Python
>>> while True: print('Hello world')
Hello world
Hello world
Hello world
Hello world
Hello world
Hello world
Hello world
Hello world
Hello world
...
```
