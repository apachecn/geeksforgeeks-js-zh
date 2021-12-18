# Lodash _ currylight 3()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-curryright3-method/](https://www.geeksforgeeks.org/lodash-_-curryright3-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_ . currylight 3()方法** r 研究了给定函数的简化版本，其中从右到左最多处理三个参数。

**语法:**

```
_.curryRight3( fun )

```

**参数:**该方法采用上面列出的单个参数，讨论如下:

*   **乐趣:**这是 curried 版本应该用到的功能。

**返回值:**这个方法返回一个 curried 函数。

**注意:**这个方法在正常的 JavaScript 中不会工作，因为它需要安装 Lodash contrib 库。可以使用 **npm 安装 lodash-contrib–保存**来安装 lodash-contrib 库

```
npm install lodash-contrib

```

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function to curry
function div(a, b, c) {
    return a / b / c;
}

var curried = _.curryRight3(div);

console.log("Curried division is :",
    curried(4)(32)(1000));
```

**输出:**

```
Curried division is : 7.8125

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function div(a, b, c) {
    return a / b / c;
}

var curried = _.curryRight3(div);

console.log("Curried division is :",
    curried(4)(1000)(10));
```

**输出:**

```
Curried division is : 0.0025

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function sub(a, b, c) {
    return a - b - c;
}

var curried = _.curryRight3(sub);

console.log("Curried Subtraction is :",
    curried(2)(10)(1000));
```

**输出:**

```
Curried Subtraction is : 988

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function div(a, b, c) {
    return ("a=" + a + " and b=" + b +
            " and c=" + c);
}

var curried = _.curryRight3(div);

console.log(curried("a")("b")("c"));
```

**输出:**

```
a=c and b=b and c=a

```