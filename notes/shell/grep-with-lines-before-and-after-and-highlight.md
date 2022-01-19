---
title: Grep with lines before and after, and highlight
tags:
  - Shell  
  - Linux
emoji: 🔍
created: 2021-03-04
modified: 2021-03-04
---

```
$ grep -B 5 -A 5 --color "Search Query"
```

For example, when I want to search for "svg fill"

```
$ git log | grep -B 4 -A 4 --color 'svg fill'
```