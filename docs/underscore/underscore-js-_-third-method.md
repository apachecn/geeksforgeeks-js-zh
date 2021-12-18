# 下划线. js _。第三种()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-third-method/](https://www.geeksforgeeks.org/underscore-js-_-third-method/)

**_。第三个()方法**获取一个数组和一个索引，并因此返回一个数组，该数组通过从原始数组中获取元素而生成，从第三个元素开始，到给定的索引结束:

**语法:**

```
_.third(array, index);
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
var arr = _.third(array, 5);
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
Generated Array:  [ -1, -1, 5 ]
```

**示例 2:** 如果没有传递索引，这个方法返回原始数组的第三个元素

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.third(array);
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
Element:  -1
```

**示例 3:** 如果传递的索引是负的，则创建的数组从右到该索引上的元素。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.third(array, -2);
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
  -1, -1,  5, 6, -6,
  -6, -7, -8, 9
]
```

**示例 4:** 如果索引超出界限，则在第三个元素之后创建剩余的完整数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating array
var arr = _.third(array, 100);
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
  -1, -1,  5, 6, -6,
  -6, -7, -8, 9,  9,
  10
]
```