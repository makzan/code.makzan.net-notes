---
title: BabelJS and JavaScript Pre-Processor
tags:
  - JavaScript
emoji: ⚙️
created: 2021-02-06
modified: 2021-02-06
---


JavaScript was inconsistent and somehow difficult to use. Throughout the years, different teams tried to solve the issue by introducing a better version of JavaScript-compatible language and then generate the JavaScript via compilation.

In the past several years, JavaScript itself has improved a lot and become much more consistent. But the version of the JavaScript release and the version that the web browser supports is not always aligned.

Babel is a unified JavaScript compiler that compiles

[https://babeljs.io](https://babeljs.io)

There are several main scenarios that we need to use Babel to compile the JavaScript.

## Modern JavaScript support in an old web browser

For example, given the following code snippet.

```js
let abc = undefined ?? "default";

let multiply = (x=1, y=1) => {
  return x*y
}
  
console.log(multiple(10,10));
console.log(multiple(10));

let obj = {
  classroom: {
    name: "JavaScript",
    year: 2021
  }
}

let class_name = obj?.classroom?.name
```


The above code works in all major modern web browsers. But that may not work for the web browser version that was released on or before 2019.

Can I Use: Optional Chain

[https://caniuse.com/?search=optional%20chain](https://caniuse.com/?search=optional%20chain)

Can I Use: Default Parameters

[https://caniuse.com/mdn-javascript_functions_default_parameters](https://caniuse.com/mdn-javascript_functions_default_parameters)

If we need to support old web browsers that were years ago. We will need to transform the modern syntax into the following, usually via Babel transpiler.

```js
var _obj$classroom;

var abc = undefined !== null && undefined !== void 0 ? undefined : "default";

var multiply = function multiply() {
  var x = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : 1;
  var y = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : 1;
  return x * y;
};

console.log(multiple(10, 10));
console.log(multiple(10));
var obj = {
  classroom: {
    name: "JavaScript",
    year: 2021
  }
};
var class_name = obj === null || obj === void 0 ? void 0 : (_obj$classroom = obj.classroom) === null || _obj$classroom === void 0 ? void 0 : _obj$classroom.name;
```