---
title: What is JSX
tags:
  - JavaScript
  - React
created: 2021-02-06
modified: 2021-02-06
---



Facebook and the React team invented the JSX syntax. It is an XML syntax to write HTML-like DOM structure. The JSX in JavaScript is transformed into createElement function.

In JSX, **everything is JavaScript**.


```js
var heading = <h1>Hello JSX</h1>;

function render() {
  let name = "JSX";
  let data = [1,2,3,4,5];
  return <App>
    <p>This is {name}</p>
      <List>
        {data.map( item => {
          <ListItem key={item}>
            content for {item}
          </ListItem>
        })}
      </List>
    </App>
}
```


JSX is a sugar syntax of the createElement function, which takes 3 or more parameters to create a structural tree of elements. The tree created is very similar to DOM tree.


```js
var heading = React.createElement("h1", null, "Hello JSX");

function render() {
  var name = "JSX";
  var data = [1, 2, 3, 4, 5];
  return React.createElement(App, null, 
    React.createElement("p", null, "This is ", name),
    React.createElement(List, null, data.map(function (item) {
      React.createElement(ListItem, {
        key: item
      }, "content for ", item);
    }))
  );
}
```


Let’s take a look at the parameters of the createElement function.

1. The first parameter is the tag name.
2. The second parameter contains the attributes of the tag if any.
3. The third parameter and so on is the content of the element.

We can use argument list to fetch the 3rd...nth argument to compose the content.

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)

Here are more JSX tutorials from FreeCodeCamp and React.

[https://www.freecodecamp.org/news/jsx-in-react-introduction/](https://www.freecodecamp.org/news/jsx-in-react-introduction/)

[https://reactjs.org/docs/introducing-jsx.html](https://reactjs.org/docs/introducing-jsx.html)