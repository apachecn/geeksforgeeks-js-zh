# 洛达什 _。splitAt()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-splitat-method/](https://www.geeksforgeeks.org/lodash-_-splitat-method/)

洛达什 T3**_。splitAt()方法** 取一个数组和一个数值索引，返回一个包含两个嵌入数组的新数组，这两个嵌入数组是通过将原始数组在提供的数值索引处拆分而成的。

**语法:**

```
_.splitAt(array, numeric_index)

```

**参数:**该方法取两个参数，如上所述，描述如下:

*   **阵:**待拆分的阵。
*   **numeric_index:** 要拆分数组的索引。

**返回值:**这个方法返回一个新创建的包含两个数组的数组。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 lodash contrib 库-保存。**

**示例 1:** 在本例中，我们将在第 4 个索引处使用此方法拆分数组。

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 3, 6, 8, 9, 11, 3];

// Value
var value = 4;

// Generating Array using splitAt() method
var arr =_.splitAt(array, value);
console.log("Array : ", array);
console.log("Numeric Value : ", value);
console.log("Generated Array : ", arr);
```

**输出:**

```
Array :  [
  1,  3, 6, 8,
  9, 11, 3
]
Numeric Value :  4
Generated Array :  [ [ 1, 3, 6, 8 ], [ 9, 11, 3 ] ]

```

**示例 2:** 在本例中，我们将在索引 0 处使用此方法拆分一个数组，因此将获得一个空数组，另一个与原始数组相同。

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 3, 6, 8, 9, 11, 3];

// Value
var value = 0;

// Generating Array using splitAt() method
var arr =_.splitAt(array, value);
console.log("Array : ", array);
console.log("Numeric Value : ", value);
console.log("Generated Array : ", arr);
```

**输出:**

```
Array :  [
  1,  3, 6, 8,
  9, 11, 3
]
Numeric Value :  0
Generated Array :  [ [], [
1, 3, 6, 8,
 9, 11, 3
] ]

```

**例 3:** 该方法对于范围外的指标是安全的。

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 3, 6, 8, 9, 11, 3];

// Value
var value = 20;

// Generating Array using splitAt() method
var arr =_.splitAt(array, value);
console.log("Array : ", array);
console.log("Numeric Value : ", value);
console.log("Generated Array : ", arr);
```

**输出:**

```
Array :  [
  1,  3, 6, 8,
  9, 11, 3
]
Numeric Value :  20
Generated Array :  [ [
1, 3, 6, 8,
 9, 11, 3
], [] ]

```