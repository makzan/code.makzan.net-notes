---
title: CSS Gradient Text
tags:
  - CSS
emoji: 🌈
created: 2020-12-05
modified: 2020-12-05
---

```css
h1 a {
  background-image: linear-gradient(to bottom right, yellow, red);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  // text-fill-color: transparent;
}
```

Demo: [codepen.io/makzan/pen/zYYObbK](https://codepen.io/makzan/pen/zYYObbK)

<iframe height="378" style="width: 100%;" scrolling="no" title="Gradient text demo" src="https://codepen.io/makzan/embed/zYYObbK?height=378&theme-id=dark&default-tab=css,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/makzan/pen/zYYObbK'>Gradient text demo</a> by Thomas Seng Hin Mak
  (<a href='https://codepen.io/makzan'>@makzan</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>