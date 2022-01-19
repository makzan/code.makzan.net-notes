---
title: Scroll-Snap
tags:
  - CSS
emoji: 🖼
created: 2019-06-02
modified: 2019-06-02
---

The `scroll-snap` CSS has [updated to new syntax](https://www.fxsitecompat.com/en-CA/docs/2019/legacy-css-scroll-snap-syntax-support-has-been-dropped/). Here is a demo of using the latest syntax of scroll-snap and also making it mobile friendly.


```html
<!-- Using different image width to demonstrate the scroll-snal-align center -->
<div class="photo-gallery">
    <img src="https://source.unsplash.com/random/500x320">
    <img src="https://source.unsplash.com/random/400x320">
    <img src="https://source.unsplash.com/random/300x320">
    <img src="https://source.unsplash.com/random/450x320">
    <img src="https://source.unsplash.com/random/400x320">
</div>

```


```css
.photo-gallery {
  width: 500px;
  max-width: 100vw;
  overflow-x: auto;
  overflow-y: hidden;
  white-space: nowrap;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
}
.photo-gallery img {
  scroll-snap-align: center;
  max-width: 100vw;
  height: 100%;
  object-fit: cover;
}
```


It also works in mobile too. You may check it out in the following demo URL:

[https://s.codepen.io/makzan/debug/EzrYXv](https://s.codepen.io/makzan/debug/EzrYXv)


## Demo

<iframe height="434" style="width: 100%;" scrolling="no" title="Testing CSS3 Scroll Snap" src="https://codepen.io/makzan/embed/EzrYXv?height=434&theme-id=light&default-tab=html,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/makzan/pen/EzrYXv'>Testing CSS3 Scroll Snap</a> by Thomas Seng Hin Mak
  (<a href='https://codepen.io/makzan'>@makzan</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>