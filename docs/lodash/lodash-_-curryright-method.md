# 洛达什 _。电流()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-curryright-method/](https://www.geeksforgeeks.org/lodash-_-curryright-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。curryRight()方法**用于 r 返回给定函数的 curryRight 版本，其中给定参数从右到左进行处理。

**语法:**

```
_.curryRight( fun )

```

**参数:**该方法采用如上所列的单个参数，讨论如下。

*   **乐趣:**这是 curried 版本应该用到的功能。

**返回值:**该方法返回 curried 函数。

**注意:**这个方法在正常的 JavaScript 中不会工作，因为它需要安装 Lodash contrib 库。可以使用 **npm 安装 lodash-contrib–保存**来安装 lodash-contrib 库

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function to curry
function div(a, b, c) {
    return a / b / c;
}

// Using the _.curryRight() method
var curried = _.curryRight(div);

console.log("Curried division is :",
    curried(3)(3)(99));
```

**输出:**

```
Curried division is : 11

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function to curry
function div(a, b, c, d) {
    return a - b - c - d;
}

// Using the _.curryRight() method
var curried = _.curryRight(div);

console.log("Curried Subtraction is :",
    curried(2)(1)(6)(44));
```

**输出:**

```
Curried Subtraction is : 35

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function to curry
function div(a, b, c) {
    return ("a=" + a + " and b=" + b +
            " and c=" + c);
}

// Using the _.curryRight() method
var curried = _.curryRight(div);

console.log(curried("a")("b")("c"));
```

**输出:**

```
a=c and b=b and c=a

```