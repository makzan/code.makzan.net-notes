---
title: Basic skeleton of web scrapping
tags:
  - Python
  - Web Scrapping
emoji: 🤖
created: 2020-07-01
modified: 2020-07-01
---

This is the skeleton of web scrapping with `BeautifulSoup`

```python
from bs4 import BeautifulSoup
import requests

url = "https://news.gov.mo/home/zh-hant"

res = requests.get(url)
soup = BeautifulSoup(res.text, "lxml")

for h5 in soup.select("h5"):
    print(h5.text.strip())

```