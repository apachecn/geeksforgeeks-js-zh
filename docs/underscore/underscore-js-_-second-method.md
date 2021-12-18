# 下划线. js _。第二种()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-秒-方法/](https://www.geeksforgeeks.org/underscore-js-_-second-method/)

_。second()方法接受一个数组和一个索引，因此返回一个数组，该数组是从原始数组中的元素开始，到给定的索引处结束而生成的:

**语法:**

```
_.second(array, index);
```

**参数:**

*   **数组:**要从元素中获取的给定数组。
*   **索引:**要获取哪些元素的索引。

**返回值:**这个方法返回一个生成的数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.second(array, 4);
console.log("Original Array : ", array);
console.log("Generated Array: ", arr);
```

**输出:**

```
Original Array :  [
   1,  2, -1, -1, 5, 6,
  -6, -6, -7, -8, 9, 9,
  10
]
Generated Array:  [ 2, -1, -1 ]
```

**示例 2:** 如果没有传递索引，这个方法返回原始数组的第二个元素

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.second(array);
console.log("Original Array : ", array);
console.log("Element: ", arr);
```

**输出:**

```
Original Array :  [
   1,  2, -1, -1, 5, 6,
  -6, -6, -7, -8, 9, 9,
  10
]
Element:  2
```

**示例 3:** 如果传递的索引是负的，则创建的数组从右到该索引上的元素。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.second(array, -2);
console.log("Original Array : ", array);
console.log("Generated Array: ", arr);
```

**输出:**

```
Original Array :  [
   1,  2, -1, -1, 5, 6,
  -6, -6, -7, -8, 9, 9,
  10
]
Generated Array:  [
   2, -1, -1,  5, 6,
  -6, -6, -7, -8, 9
]
```

**示例 4:** 如果索引超出界限，则在第二个元素之后创建剩余的完整数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.second(array, 100);
console.log("Original Array : ", array);
console.log("Generated Array: ", arr);
```

**输出:**

```
Original Array :  [
   1,  2, -1, -1, 5, 6,
  -6, -6, -7, -8, 9, 9,
  10
]
Generated Array:  [
   2, -1, -1,  5, 6,
  -6, -6, -7, -8, 9,
   9, 10
]
```