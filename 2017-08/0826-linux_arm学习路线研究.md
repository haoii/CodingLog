---
date: 2017-08-26 14:23
status: public
title: linux_arm学习路线研究
---

1. s3c2410还是Exynos4412处理器, 还是DSP
2. bootloader(uBoot), BIOS
3. linux驱动开发

## 系统开发
1. 硬件
    1. 原理图
    2. layout
    3. bootloader
        - uBoot（iRom，BL1, BL2, uBoot）
2. 驱动
3. 应用

## uBoot
1. uboot开发
2. BL1, BL2, uBoot, 三星自己提供的uBoot
3. 针对同一个cpu的uBoot一样吗？为什么需要一直uBoot？
4. BSP开发包含什么

## 问题
1. 编译器的界限，程序的起始？
2. uBoot和kernel的接口