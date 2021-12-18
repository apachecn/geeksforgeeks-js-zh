# 洛达什 _。overArgs()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-overargs-method/](https://www.geeksforgeeks.org/lodash-_-overargs-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。overrgs()****方法**用于创建一个调用*函数*的函数，其参数使用给定的*变换*函数进行变换。

**语法:**

```
_.overArgs(func, transforms )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **功能:**此参数保存要包装的功能。
*   **转换:**此参数保存指定参数转换的函数。这是一个可选参数。

**返回值:**该方法返回新函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Function to calculate the
// Cube of a number
function Cube(number) {
  return number * number * number;
}

// Function to calculate the
// triple value of a number
function Triple(number) {
  return number * 3;
}

// Using the _.overArgs() method 
var func = _.overArgs(function(a, b) {
  return [a, b];
}, [Cube, Triple]);

// print the output
console.log(func(3, 5));
```

**输出:**

```
[27, 15]
```

**例 2:**

## java 描述语言

```
// Function to calculate the
// double value of a number
function doubled(number) {
  return number * 2;
}

// Function to calculate the
// square value of a number
function square(number) {
  return number * number;
}

// Using the _.overArgs() method 
var func = _.overArgs(function(a, b) {
  return [a, b];
}, [square, doubled]);

// print the output
console.log(func(5, 8));
```

**输出:**

```
[25, 16]
```