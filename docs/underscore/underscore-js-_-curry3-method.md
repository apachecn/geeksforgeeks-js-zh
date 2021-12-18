# 下划线. _ .curry3()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-curry3-method/](https://www.geeksforgeeks.org/underscore-js-_-curry3-method/)

方法 r 是给定的函数的 current 版本，但是将精确地处理三个参数，不多也不少。

**语法:**

```
_.curry3( fun )

```

**参数:**该方法采用上面列出的单个参数，讨论如下:

*   **趣味:**这是作为参数传递的给定函数。

**返回值:**返回函数的 curried 版本。

**注意:**要执行以下示例，您必须使用此命令提示符安装**下划线-contrib** 库，并执行以下命令。

```
npm install underscore-contrib

```

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b, c) {
    return a*b*c;
}

// Making curried function
var gfgFunc = _.curry3(fun);

// Only operates for exactly two arguments
console.log("Multiplication is :", 
    gfgFunc(20)(23)(2));
```

**输出:**

```
Multiplication is : 920

```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b, c) {
    return a-b-c;
}

// Making curried function
var gfgFunc = _.curry3(fun);

// Only operates for exactly two arguments
console.log("Subtraction is :", 
    gfgFunc(25)(23)(1));
```

**输出:**

```
Subtraction is : 1
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(x, y, z) {
    return arguments;
}

// Making curried function
var gfgFunc = _.curry3(fun);

// Only operates for exactly three arguments
console.log("Curried Arguments are :", 
    gfgFunc("a")("b")("c"));
```

**输出:**

```
Curried Arguments are : [Arguments] { '0': 'a', '1': 'b', '2': 'c' }
```

**例 4:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(x, y, z) {
    return arguments;
}

// Making curried function
var gfgFunc = _.curry3(fun);

// Only operates for exactly three arguments
// For two args, it returns function
console.log(gfgFunc("a")("b"));
```

**输出:**

```
[Function: mustBeUnary]

```