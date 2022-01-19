---
title: Flexbox-based Mobile-first CSS Layout
tags:
  - CSS
emoji: 🪟
created: 2021-04-30
modified: 2021-04-30
---

This is a mobile-first row-columns layout that uses Flexbox.

```css
*{box-sizing: border-box;}
img {max-width: 100%;}
.row {
  display: flex;
  flex-wrap: wrap;
}
.row .row {
  margin-left: -.5em;
  margin-right: -.5em;
}
.col {
  flex: 0 1 100%;
  padding: 0 .5em;
}
.small-1 {flex: 0 1 calc(100% / 12 * 1)}
.small-2 {flex: 0 1 calc(100% / 12 * 2)}
.small-3 {flex: 0 1 calc(100% / 12 * 3)}
.small-4 {flex: 0 1 calc(100% / 12 * 4)}
.small-5 {flex: 0 1 calc(100% / 12 * 5)}
.small-6 {flex: 0 1 calc(100% / 12 * 6)}
.small-7 {flex: 0 1 calc(100% / 12 * 7)}
.small-8 {flex: 0 1 calc(100% / 12 * 8)}
.small-9 {flex: 0 1 calc(100% / 12 * 9)}
.small-10 {flex: 0 1 calc(100% / 12 * 10)}
.small-11 {flex: 0 1 calc(100% / 12 * 11)}
.small-12 {flex: 0 1 calc(100% / 12 * 12)}
.small-shrink { flex: 0 1 auto; }
.small-auto { flex: 1; }
.small-hidden {display: none;}
.small-horizontal { flex-direction: row; }
.small-vertical { flex-direction: column; }

.show-in-small-only {}
.show-in-medium-only { display: none; }
.show-in-large-only { display: none; }

@media screen and (min-width: 550px) {
  .small-hidden {display: block;}
  .show-in-small-only {display: none;}
  .show-in-medium-only { display: block; }
  .show-in-large-only { display: none; }


  .medium-1 {flex: 0 1 calc(100% / 12 * 1)}
  .medium-2 {flex: 0 1 calc(100% / 12 * 2)}
  .medium-3 {flex: 0 1 calc(100% / 12 * 3)}
  .medium-4 {flex: 0 1 calc(100% / 12 * 4)}
  .medium-5 {flex: 0 1 calc(100% / 12 * 5)}
  .medium-6 {flex: 0 1 calc(100% / 12 * 6)}
  .medium-7 {flex: 0 1 calc(100% / 12 * 7)}
  .medium-8 {flex: 0 1 calc(100% / 12 * 8)}
  .medium-9 {flex: 0 1 calc(100% / 12 * 9)}
  .medium-10 {flex: 0 1 calc(100% / 12 * 10)}
  .medium-11 {flex: 0 1 calc(100% / 12 * 11)}
  .medium-12 {flex: 0 1 calc(100% / 12 * 12)}
  .medium-shrink { flex: 0 1 auto; }
  .medium-auto { flex: 1; }
  .medium-hidden {display: none;}  
  .medium-horizontal { flex-direction: row; }
  .medium-vertical { flex-direction: column; }

  .medium-order-1 {order: 1;}
  .medium-order-2 {order: 2;}
  .medium-order-3 {order: 3;}
  .medium-order-4 {order: 4;}
  .medium-order-5 {order: 5;}
  .medium-order-6 {order: 6;}
  .medium-order-7 {order: 7;}
  .medium-order-8 {order: 8;}
  .medium-order-9 {order: 9;}
  .medium-order-10 {order: 10;}
  .medium-order-11 {order: 11;}
  .medium-order-12 {order: 12;}
}

@media screen and (min-width: 850px) {
  .medium-hidden {display: block;}
  .show-in-small-only {display: none;}
  .show-in-medium-only { display: none; }
  .show-in-large-only { display: block; }


  .large-1 {flex: 0 1 calc(100% / 12 * 1)}
  .large-2 {flex: 0 1 calc(100% / 12 * 2)}
  .large-3 {flex: 0 1 calc(100% / 12 * 3)}
  .large-4 {flex: 0 1 calc(100% / 12 * 4)}
  .large-5 {flex: 0 1 calc(100% / 12 * 5)}
  .large-6 {flex: 0 1 calc(100% / 12 * 6)}
  .large-7 {flex: 0 1 calc(100% / 12 * 7)}
  .large-8 {flex: 0 1 calc(100% / 12 * 8)}
  .large-9 {flex: 0 1 calc(100% / 12 * 9)}
  .large-10 {flex: 0 1 calc(100% / 12 * 10)}
  .large-11 {flex: 0 1 calc(100% / 12 * 11)}
  .large-12 {flex: 0 1 calc(100% / 12 * 12)}
  .large-shrink { flex: 0 1 auto; }
  .large-auto { flex: 1; }
  .large-hidden {display: none;}
  .large-horizontal { flex-direction: row; }
  .large-vertical { flex-direction: column; }

  .large-order-1 {order: 1;}
  .large-order-2 {order: 2;}
  .large-order-3 {order: 3;}
  .large-order-4 {order: 4;}
  .large-order-5 {order: 5;}
  .large-order-6 {order: 6;}
  .large-order-7 {order: 7;}
  .large-order-8 {order: 8;}
  .large-order-9 {order: 9;}
  .large-order-10 {order: 10;}
  .large-order-11 {order: 11;}
  .large-order-12 {order: 12;}
}
```