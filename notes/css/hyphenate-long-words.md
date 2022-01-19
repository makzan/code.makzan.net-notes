---
title: Dealing with long words in CSS
emoji: 💬
tags:
  - CSS
created: 2015-09-25
modified: 2015-09-25
link: https://justmarkup.com/log/2015/07/31/dealing-with-long-words-in-css/
---

Link: [Dealing with long words in CSS](https://justmarkup.com/log/2015/07/31/dealing-with-long-words-in-css/)

> Final solution
> 
> This solution will show hyphens for every browser supporting it and will break lines in every other browser – perfect.
This is a useful technique when you need to deal with long words in your web design. For example, when you need to reference a long city name.

```css
.hyphenate {
  overflow-wrap: break-word;
  word-wrap: break-word;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;
  -moz-hyphens: auto;
  hyphens: auto;
}
```