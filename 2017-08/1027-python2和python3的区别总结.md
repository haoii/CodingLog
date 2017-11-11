---
date: 2017-10-27 19:27
status: public
title: 1027-python2和python3的区别总结
---

## 区别
1. （tutorial - 3.1.1）py3中 17 / 5 = 3.4， 17 // 5 = 3
2. （tutorial - 3.1.3）unicode问题：待定
3. （tutorial - 4.3）py3中range()函数产生range对象，py2中则产生list对象。
4. （tutorial - 4.x）Function Annotations：待定
5. （tutorial - 5.1）py3中list增加clear、copy函数，修改index函数。
6. （tutorial - 5.1.3）py3中map、filter、reduce函数变化：待定
7. （tutorial - 5.6）循环dict的iteritems()函数变更为items()函数
8. （tutorial - 5.8）不同类型对象的比较，变更为：只有定义了比较函数才能比较；数值类型按照数值大小比较，如 0== 0.0。
9. （tutorial - 6.1.3）（tutorial - 6.1.3）（tutorial - 6.4.2）

## py3文档修改内容
1. （tutorial - 4.3）list(range(10)) = [0,1,2,3,4,5,6,7,8,9]
2. （tutorial - 4.7.3）变长变量之后只能跟关键字变量
3. （tutorial - 5.1.3）for循环之后，循环变量i依然存在。
4.