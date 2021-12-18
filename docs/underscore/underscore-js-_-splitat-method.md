# 下划线. js _。splitAt()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-splitat-method/](https://www.geeksforgeeks.org/underscore-js-_-splitat-method/)

****_。splitAt()方法** 获取一个数组和一个数值索引，并返回一个包含两个数组的新数组，这两个数组是通过在提供的数值索引处拆分原始数组而得到的。**

****语法:****

```
_.splitAt(array, numeric_index) 
```

****参数:****

*   ****阵:**待拆分的阵。**
*   ****numeric_index:** 要拆分数组的索引。**

****返回值:**这个方法返回一个新创建的包含两个数组的数组。**

****注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。****

****示例 1:** 在本例中，我们将在索引 3 处使用此方法拆分数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array
var array = [1, 3, 6, 8, 9, 11, 3];

// Value
var value = 3;

// Generating Array using splitAt() method
var arr =_.splitAt(array, value);
console.log("Array : ", array);
console.log("Numeric Value : ", value);
console.log("Generated Array : ", arr);
```

****输出:****

```
Array :  [
  1,  3, 6, 8,
  9, 11, 3
]
Numeric Value :  3
Generated Array :  [ [ 1, 3, 6 ], [ 8, 9, 11, 3 ] ] 
```

****示例 2:** 在本例中，我们将在索引 0 处使用此方法拆分一个数组，因此将获得一个空数组和一个与原始数组相同的数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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

****输出:****

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

****例 3:** 该方法对于范围外的指标是安全的。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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

****输出:****

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