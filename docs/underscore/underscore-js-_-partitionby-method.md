# 下划线. js _。partitionBy()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-partitionby-method/](https://www.geeksforgeeks.org/underscore-js-_-partitionby-method/)

**_。partitionBy()方法**获取一个数组和一个函数，并根据给定函数的条件生成一个分区数组。

**语法:**

```
_.partitionBy(array, function)
```

**参数:**

*   **数组:**要从中创建分区数组的给定数组。
*   **函数:**包含数组分区条件的函数。

**返回值:**这个方法返回一个新创建的分区数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contribute 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 在本例中，我们将使用此方法创建奇偶元素的分区数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, 3, 2, 1, 1, 5, 6, 6, 6, 7, 8, 9, 9, 10];
// Creating partitioned array
var p_arr = _.partitionBy(array, _.isOdd);
console.log("Original Array : ", array);
console.log("Partitioned Arrayy: ", p_arr);
```

**输出:**

```
Original Array :  [
  1, 2,  3, 2, 1, 1,
  5, 6,  6, 6, 7, 8,
  9, 9, 10
]
Partitioned Arrayy:  [
  [ 1 ],       [ 2 ],
  [ 3 ],       [ 2 ],
  [ 1, 1, 5 ], [ 6, 6, 6 ],
  [ 7 ],       [ 8 ],
  [ 9, 9 ],    [ 10 ]
]
```

**示例 2:** 在本例中，我们将创建一个所有相同元素的分区数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, 3, 2, 1, 1, 5, 6, 6, 6, 7, 8, 9, 9, 10];
// Creating partitioned array
var p_arr = _.partitionBy(array, _.identity);
console.log("Original Array : ", array);
console.log("Partitioned Arrayy: ", p_arr);
```

**输出:**

```
Original Array :  [
  1, 2,  3, 2, 1, 1,
  5, 6,  6, 6, 7, 8,
  9, 9, 10
]
Partitioned Arrayy:  [
  [ 1 ],       [ 2 ],
  [ 3 ],       [ 2 ],
  [ 1, 1 ],    [ 5 ],
  [ 6, 6, 6 ], [ 7 ],
  [ 8 ],       [ 9, 9 ],
  [ 10 ]
]
```

**示例 3:** 在本例中，我们将创建一个包含所有负数和正数的分区数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1, 2, 3, 2, -1, -1, 5, 6, -6, -6, -7, -8, 9, 9, 10];
// Creating partitioned array
var p_arr = _.partitionBy(array, function(val) {
  return val>0
});
console.log("Original Array : ", array);
console.log("Partitioned Arrayy: ", p_arr);
```

**输出:**

```
Original Array :  [
  1, 2,  3,  2, -1, -1,
  5, 6, -6, -6, -7, -8,
  9, 9, 10
]
Partitioned Arrayy:  [
  [ 1, 2, 3, 2 ],
  [ -1, -1 ],
  [ 5, 6 ],
  [ -6, -6, -7, -8 ],
  [ 9, 9, 10 ]
]
```