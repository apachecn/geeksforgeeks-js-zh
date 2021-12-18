# 洛达什 _。partitionBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-partitionby-method/](https://www.geeksforgeeks.org/lodash-_-partitionby-method/)

**洛达什 _。partitionBy()方法**获取一个数组和一个函数，并根据给定函数的条件生成一个分区数组。

**语法:**

```
_.partitionBy(array, function)

```

**参数:**该方法取两个参数，如上所述，描述如下:

*   **数组:**要从中创建分区数组的给定数组。
*   **函数:**包含数组分区条件的函数。

**返回值:**这个方法返回一个新创建的分区数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash.js contribute 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Declare an array 
var array = [1, 2, 3, 2, 1, 1, 
    5, 6, 6, 6, 7, 8, 9, 9, 10]; 

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

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Declare an array 
var array = [1, 2, 3, 2, 1, 1, 
    5, 6, 6, 6, 7, 8, 9, 9, 10]; 

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

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Declare an array 
var array = [1, 2, 3, 2, -1, -1, 5, 
        6, -6, -6, -7, -8, 9, 9, 10];

// Creating partitioned array 
var p_arr = _.partitionBy(array, function(val) { 
  return val > 0 
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