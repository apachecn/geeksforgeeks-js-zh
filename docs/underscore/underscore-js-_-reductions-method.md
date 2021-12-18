# 下划线. js _。减量()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-reductions-method/](https://www.geeksforgeeks.org/underscore-js-_-reductions-method/)

**_。reductions()** 方法用于将元素数组转换为 数组，其中存储了折叠操作中的每个中间值。这个方法是同 _。方法，只是它返回一个数组。

一个数组、一个函数、和一个起始值在该方法中被传递，以生成一个新的数组来对和数组执行操作。

**语法:**

```
_.reductions(array, function, start_val)
```

**参数:**

*   **数组:**要处理的数组。
*   **函数:**包含迭代条件的函数。
*   **start_val:** 在开始时传递的值，该值在后续操作中进一步更新。

**返回值:**这个方法返回一个新数组。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。 可以使用 `npm install underscore-contrib --save.`安装下划线. js contrib 库

**示例 1:** 在本例中，我们将使用此方法生成一个数组。这里，求和数组是用给定的起始值 0 生成的，该值在加法运算时更新。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Defining Array
var array = [10, 12, 23, 34, 45];

var arr =_.reductions(array, function(st, n) {
  return st + n;
}, 0);
console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[ 10, 22, 45, 79, 124 ]
```

**示例 2:** 在本例中，我们将通过将起始值设为 1 来生成乘法数组，该值在进一步乘法时更新。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Defining Array
var array = [10, 12, 23, 34, 45];

var arr =_.reductions(array, function(st, n) {
  return st * n;
}, 1);
console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[ 10, 120, 2760, 93840, 4222800 ]

```