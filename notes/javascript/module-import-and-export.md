---
title: JavaScript Import and Export Module
tags:
  - JavaScript
emoji: ⤵️
created: 2021-02-06
modified: 2021-02-06
---



When our project gets bigger, we want to divide and modularize our code into smaller pieces in order for easier maintenance.

utils.js

```js
/* Test JavaScript Export */

export default function mul(x=1, y=1) {
  return x*y
}
```


main.js

```js
import mul from './utils.js'

console.log("Hello")

console.log(mul(10,10));

document.querySelector("#result").textContent = mul(10,10);
```


index.html

```js
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Test JavaScript Export/Import</title>
  </head>
  <body>
    <p>Result: <span id="result">...</span></p>
    <script type="module" src="utils.js"></script>
    <script type="module" src="main.js"></script>
  </body>
</html>
```


[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)