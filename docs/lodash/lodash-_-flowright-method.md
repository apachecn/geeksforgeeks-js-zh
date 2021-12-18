# 洛达什 _。flowRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flowright-method/](https://www.geeksforgeeks.org/lodash-_-flowright-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。flowRight()** **方法**用于创建一个新的复合函数，该函数从右向左调用所提供的函数，其中每个连续的调用都被提供上一个调用的返回值。几乎和 _。flow()方法。

**语法:**

```
_.flowRight( funcs )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **函数:**该参数保存要调用的函数。这是一个可选参数。

**返回值:**该方法返回新的复合函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Function to calculate the
// Cube of a number
function cube(number) {
  return number * number * number;
}

// Using the _.flowRight() method 
var multiplycube =
 _.flowRight([cube, _.multiply]);

// Printing the output
console.log(multiplycube(2, 3));
```

**输出:**

```
216
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Function to calculate the
// double value of a number
function doubled(number) {
  return number * 2;
}

// Using the _.flowRight() method 
var adddoubled =
  _.flowRight([doubled, _.add]);

// Printing the output
console.log(adddoubled(6, 8));
```

**输出:**

```
28 
```