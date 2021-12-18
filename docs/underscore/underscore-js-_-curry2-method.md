# 下划线. _ .curry2()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-curry2-method/](https://www.geeksforgeeks.org/underscore-js-_-curry2-method/)

方法 r 使用了给定的函数的 current 版本，但是将使用两个参数，不多也不少。

**语法:**

```
_.curry2( fun )

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
function fun(a, b) {
    return a*b;
}

// Making curried function
var gfgFunc = _.curry2(fun);

// Only operates for exactly two arguments
console.log("Multiplication is :", 
    gfgFunc(20)(23));
```

**输出:**

```
Multiplication is : 460

```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b) {
    return a-b;
}

// Making curried function
var gfgFunc = _.curry2(fun);

// Only operates for exactly two arguments
console.log("Subtraction is :", 
    gfgFunc(25)(23));
```

**输出:**

```
Subtraction is : 2

```

**示例 3:** 打印 curry2()函数获取的参数。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(x, y) {
    return arguments;
}

// Making curried function
var gfgFunc = _.curry2(fun);

// Only operates for exactly two arguments
console.log("Curried Arguments are :", 
    gfgFunc("a")("b"));
```

**输出:**

```
Curried Arguments are : [Arguments] { '0': 'a', '1': 'b' }

```