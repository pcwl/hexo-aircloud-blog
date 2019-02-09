---
title: Mac 写入镜像到 sd 卡
date : 2018-10-24 16:45:11
tag:
    - Mac
    - RaspberryPi
---

### Mac 写入镜像到 sd 卡

##### 可通过此方法制作 win 启动盘或给 Raspberry Pi 刷系统

##### 步骤

*   如果 U 盘需要格式化，可用磁盘工具处理

*   查看挂载位置

    ```
    diskutil list
    ```

*   卸载设备

    ```
    diskutil unmountDisk
    ```

*   用 dd 命令写入镜像

    ```
    sudo dd bs=1m if=目标镜像 of=设备位置
    ```

    过程中 ctrl + t 可查看进度

*   写入完毕后卸载或弹出设备就可以使用了

##### 树莓派官方 Mac 下烧录指导

[链接](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md)
