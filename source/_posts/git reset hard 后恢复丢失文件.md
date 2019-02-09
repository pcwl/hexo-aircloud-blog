---
title: git reset hard 后恢复丢失文件
date : 2019-02-09 15:18:31
tag:
    - git
---

### 起因

很长时间没动博客，之前用的 hexo 模版有更新，由于冲突无法直接 pull。打算 fock 到自己到仓库跟踪，不小心没备份之前的文章就进行 git reset hard。“道路千万条，安全第一条，行车不规范，唯有泪两行“，结果坑了自己一把，又一次爬坑中学习。

### 要点

git add 文件后，误操作 git reset hard 到之前版本，导致文件丢失。

### 文件找回方法

1. 执行如下命令
```
find .git/objects -type f | xargs ls -lt | sed 60q
```

2. 到以下路径

.git/lost-found/other

3. mac 预览的话已经可以看出是图片文件或者 markdown 文件，剩下的就是拷贝出来改成需要的名字，问题解决，出坑。

[参考](https://www.cnblogs.com/hope-markup/p/6683522.html)