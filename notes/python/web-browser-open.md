---
title: WebBrowser.open
tags:
  - Python
emoji: 🌏
created: 2020-07-01
modified: 2020-07-01
---

Opening web browser with Python


```python
import webbrowser

query = "Python history"

url = f"https://duckduckgo.com?q=!+{query}"

webbrowser.open(url)
```