# 洛达什 _。方法()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-method-method/](https://www.geeksforgeeks.org/lodash-_-method-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。method()** 方法创建一个函数，该函数在给定对象的路径上调用方法。任何额外的参数都被提供给被调用的方法。

**语法:**

```
_.method(path, args)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **路径:**这是调用的路径。
*   **参数:**这些是调用方法的参数。

**返回值:**这个方法返回新的调用者函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.method() method 
var gfg = [
    { 'a': { 'b': _.constant("geeks") } },
    { 'a': { 'b': _.constant("for") } },
    { 'a': { 'b': _.constant("geeks") } }
];

let ans = _.map(gfg, _.method('a.b'));

// Printing the output  
console.log(ans);
```

**输出:**

```
["geeks", "for", "geeks"]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.method() method 
var gfg =[ 
    { 'b': _.constant(1) }, 
    { 'b': _.constant(5) },
    { 'b': _.constant(8) }
];

let ans = _.map(gfg, _.method(['b']));

// Printing the output  
console.log(ans);
```

**输出:**

```
[1, 5, 8]

```