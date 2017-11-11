---
date: 2017-10-17 15:38
status: public
title: 1017-python_import总结
---

## 原理
1. 不论哪一种语法，都按以下两步（可能反复执行）：
    * step1：查找模块； 
    * step2：添加局部标识符表（局部变量表）

## 语法
1. `import module/package` 或 `from rela_package import package/module/`：
    * 将`module/package`标识符添加到当前局部标识符表。前者可能是很长的全路径；后者是单独模块名，但容易发生冲突。
    * `package`标识符只能访问其`__init__.py`内部的局部标识符（即其属性），并且不受其是否定义`__all__`影响。
2. `from package import *`：
    * 若其`__init__.py`没有定义`__all__`，则将`__init__.py`内部的局部标识符（除了以'_'开头的）（即其属性）添加到当前局部标识符表。
    * 若其`__init__.py`定义了`__all__`，则将`__all__`中定义的所有标识符添加到当前局部标识符表，不添加`__all__`中没有定义的其他局部标识符。
        * `__all__`为字符串list，只能是`__init__.py`所在文件夹（不包括子文件夹）中的其他模块名，或者`__init__.py`内部的局部标识符。
        * `__all__`可以设计为API接口，并且可以减少模块的重复无用导入。 
3. `from module import item/*`：
    * 基本类似于上一条。

## 其他
1. `import xxx`之后总可以跟`as xx`作为缩写。
2. 无论哪个语法，总是只在第一次导入某个module或package（导入这个module或者其中的一部分项）时，执行module或package的`__init__.py`中的全局语句。

