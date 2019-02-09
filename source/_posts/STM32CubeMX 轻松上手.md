---
title: STM32CubeMX 轻松上手
date : 2018-11-02 10:16:34
tag:
    - STM32
    - STM32CubeMX
---

### 简介

STM32CubeMX 是 ST 官方的图形化配置工具，可生成多种 IDE 代码，高效完成 STM32 系列芯片初始化配置。

### 缘由

官方相关文档较多且不易查找，这边整理后，清晰记录相关信息，方便之后环境迁移。

### 软件官方链接

STM32CubeMX 图形配置工具 [官链](https://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-configurators-and-code-generators/stm32cubemx.html)

需要值得注意的是：
- 代码生成功能需要对应芯片类型的包，链接中包含配置工具及各系列芯片包
- 中文官网更像是一个文件中转，查找各种包及软件不很方便

### 开始动手

- 下软件，下包，装软件，从本地装包（在线装不好用）。

- 新建工程（保存路径最好不要有中文和特殊字符），选芯片，配 SYS 中的 Debug。

- 生成代码（第一次会跳出工程设置，可设置项目名称、路径和生成代码对应的 IDE），其实这样就可以生成最小化代码了。

- 生成成功后跳出打开工程，进入并编译，没出问题的话就可以迭代了～

以上相关操作官方的帮助文档都有较详细的说明。（F1 快速打开帮助）

### 问题

包含中文路径或者特殊字符，生成 MDK 代码会出问题，导入不了 .s 文件，无法编译通过。[参考](https://community.st.com/s/question/0D50X00009XkWJBSA3/cubemx-project-generation-have-problem)
