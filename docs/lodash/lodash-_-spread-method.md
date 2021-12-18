# 洛达什 _。价差()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-spread-method/](https://www.geeksforgeeks.org/lodash-_-spread-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。spread()方法**用于创建一个函数，该函数使用创建函数的*这个*绑定以及一个参数数组来调用给定的函数作为参数。它基于 JavaScript 中的扩展运算符。

**语法:**

```
_.spread( func, start )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **func:** 是用来展开参数的函数。
*   **开始:**是价差的开始位置。这是一个可选参数。默认值为 0。

**返回值:**该方法返回新函数。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.spread() method with its parameter
var write = _.spread(function(author, portal) {
  return author + ' writes for ' + portal + '!';
});

// Calling write with its values
write(['Nidhi', 'GeeksforGeeks']);
```

**输出:**

```
Nidhi writes for GeeksforGeeks!

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.spread() method with its parameter
var addition = _.spread(function(x, y) {
  return x + y;
});

// Calling addition with its values
addition([56, 44]);
```

**输出:**

```
100

```