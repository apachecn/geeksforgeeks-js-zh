# 下划线. js _。takeSkipping()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-takeskipping-method/](https://www.geeksforgeeks.org/underscore-js-_-takeskipping-method/)

****_。take skip()方法** 取一个数组和一个 skip 值(比如 n)，创建一个包含原数组每第 n 个元素的数组。**

**对于一个索引>= 0的第一个元素新数组总是与相同的第一个元素原始数组。**

****语法:****

```
_.takeSkipping(array, skip_value) 
```

****参数:****

*   ****数组:**要制作跳过数组的数组。**
*   ****skip_value:** 用于从原始数组制作 skip 数组的值。**

****返回值:**这个方法返回一个新创建的跳过数组。**

****注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。****

****示例 1:** 在本例中，我们将使用此方法生成一个跳过数组。**

## **java 描述语言**

```
// Defining underscore contrib variable

var _ = require('underscore-contrib'); 
// Array

var array = [1, 2, 3, 4, 6, 4, 3, 10];

// skipValue
var skip = 2;

// Generating Array using takeSkipping() method
var arr =_.takeSkipping(array, skip);
console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

****输出:**生成的跳过数组包含第(n+2)个索引元素。**

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  2
Generated Array :  [ 1, 3, 6, 3 ] 
```

****示例 2:** 该方法对于大于或小于数组大小的跳过值是安全的。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array
var array = [1, 2, 3, 4, 6, 4, 3, 10];

// skipValue
var skip = 20;

// Generating Array using takeSkipping() method
var arr =_.takeSkipping(array, skip);
console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

****输出:**生成的数组中只有第一个元素或第 0 个索引元素。**

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  2
0
Generated Array :  [ 1 ] 
```

****示例 3:** 对于负跳过值，它返回一个空数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array
var array = [1, 2, 3, 4, 6, 4, 3, 10];

// skipValue
var skip = -20;

// Generating Array using takeSkipping() method
var arr =_.takeSkipping(array, skip);
console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

****输出:****

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  -20
0
Generated Array :  [] 
```