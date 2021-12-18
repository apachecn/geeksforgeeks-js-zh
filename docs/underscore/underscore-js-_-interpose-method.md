# 下划线. js _。插入()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-inter-method/](https://www.geeksforgeeks.org/underscore-js-_-interpose-method/)

**_。interpose()方法**获取一个数组和一个元素，并返回一个新的数组，给定的元素插入到原始数组的每个元素之间。

**语法:**

```
_.interpose(array, element)
```

**参数:**

*   **数组:**要插入元素的数组。
*   **元素:**每隔一个元素插入的元素。

**返回值:**这个方法返回一个新创建的插入数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–保存**来安装下划线. js contrib 库

**示例 1:** 在本例中，我们将使用此方法创建一个新数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var arr = [8, 8, 8, 8, 8, 8];
// Element
var ele = 0
// Constructing interposed array
var i_arr = _.interpose(arr, ele);
console.log("Array : ");
console.log(arr);
console.log("Element : ");
console.log(ele);
console.log("Interposed array : ");
console.log(i_arr);
```

**输出:**

```
Array :
[ 8, 8, 8, 8, 8, 8 ]
Element :
0
Interposed array :
[
  8, 0, 8, 0, 8,
  0, 8, 0, 8, 0,
  8
]

```

**例 2:** 如果没有介数，则返回原始数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var arr = [8];
// Element
var ele = 0
// Constructing interposed array
var i_arr = _.interpose(arr, ele);
console.log("Array : ");
console.log(arr);
console.log("Element : ");
console.log(ele);
console.log("Interposed array : ");
console.log(i_arr);
```

**输出:**这里，由于元素不足，对组块数组进行了补偿。

```
Array :
[ 8 ]
Element :
0
Interposed array :
[ 8 ]

```

**例 3:** 对于空数组，返回相同的空数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var arr = [];
// Element
var ele = 0
// Constructing interposed array
var i_arr = _.interpose(arr, ele);
console.log("Array : ");
console.log(arr);
console.log("Element : ");
console.log(ele);
console.log("Interposed array : ");
console.log(i_arr);
```

**输出:**这里，由于元素不足，对组块数组进行了补偿。

```
Array :
[ 0 ]
Element :
0
Interposed array :
[ 0 ]

```