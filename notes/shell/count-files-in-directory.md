---
title: Counting files in directory
tags:
  - Shell  
  - Linux
emoji: 🔍
created: 2021-03-05
modified: 2021-03-05
---

Count all files in current directory.

```
$ ls -l | wc -l
```

Count all files, including sub-directories.

```
$ find . -type f | wc -l
```

