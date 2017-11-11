---
date: 2017-10-28 00:50
status: public
title: 1028-XML_JSON_SQLite
---

1. 都是客户端数据存储，服务端一般用其他非嵌入式数据库（MySQL、DB2）
2. 少量数据用xml；很多数据，且需要查询，要考虑速度效率等使用SQLite
3. 网络相关使用JSON，JSON相比xml更简单