---
title: Disabling ONLY_FULL_GROUP_BY sql_mode
tags:
  - MySQL
emoji: ⚙️
created: 2020-10-12
modified: 2020-10-12
---

```mysql
SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''))
```