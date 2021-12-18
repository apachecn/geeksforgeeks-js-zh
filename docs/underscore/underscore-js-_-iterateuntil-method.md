# 下划线. js _。迭代直到()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代直到-method/](https://www.geeksforgeeks.org/underscore-js-_-iterateuntil-method/)

**_。迭代直到()** **方法**采用两个函数，一个用作结果生成器，另一个用作停止检查和种子值 say n，并返回每个生成结果的数组。的操作 _。迭代直到()方法是这样的，结果生成器在开始时传递种子值，后续的每个结果将继续 **直到** 结果未通过检查功能。

生成器函数被馈送起始种子值，因此生成数组，直到停止检查函数返回 **false** 。

**语法:**

```
_.iterateUntil(genFunc, checkFunc, seed_val)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **genFunc:** 该函数用作结果生成器。
*   **检查功能:**用作停止检查的功能。
*   **seed_val:** 启动时传递给发电机的值。

**返回值:**这个方法返回一个生成的数组。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js **contrib** 库。

可以使用 **npm 安装下划线-contrib–保存**来安装下划线. js **contrib** 库

**示例 1:** 在本例中，我们将使用此方法生成一个数组。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Defining Generating function
var genFunc = 
function(n) { 
    return n + 1; 
}
// Defining stop-check function
var checkFunc = 
function(n) { 
    return n < 11; 
}
// Generating an array
var arr = _.iterateUntil(genFunc, checkFunc, 1);
console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[
  2, 3, 4,  5, 6,
  7, 8, 9, 10
]

```

**示例 2:** 在本例中，我们将通过给定种子值 0 并从生成函数返回 n+2，使用此方法生成一个 2 的表的数组。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Defining Generating function
var genFunc = 
function(n) { 
    return n + 2; 
}
// Defining stop-check function
var checkFunc = 
function(n) { 
    return n < 21; 
}
// Generating an array
var arr = _.iterateUntil(genFunc, checkFunc, 0);
console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[
   2,  4,  6,  8, 10,
  12, 14, 16, 18, 20
]    

```