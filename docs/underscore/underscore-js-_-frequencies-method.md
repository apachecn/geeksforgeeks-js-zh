# 下划线. js _。频率()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-频率-方法/](https://www.geeksforgeeks.org/underscore-js-_-frequencies-method/)

**_。frequencies()方法**获取一个数组，r 返回一个映射对象，其键是数组的元素的值，而值是该数组中出现的键的计数。

**语法:**

```
_.frequencies( array );

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **Array:** The given array from which the mapping is to be created.

**返回值:**这个方法返回一个创建的映射对象。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = ["Geeks", "Geeks", "GFG", 
             "Computer_Science_Portal", 
             "Geeks", "GFG"];

var obj = _.frequencies(array);
console.log("Original Array : ", array);
console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Original Array :  [ 'Geeks', 'Geeks', 'GFG', 
'Computer_Science_Portal', 'Geeks', 'GFG' ]
Generated Mapping Object:  { Geeks: 3, GFG: 2, 
Computer_Science_Portal: 1 }

```

**示例 2:** 对于空数组，创建一个空对象。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [];

var obj = _.frequencies(array);
console.log("Original Array : ", array);
console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Original Array :  []
Generated Mapping Object:  {}

```

**示例 3:** 该方法适用于整数数组。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [1,1,1,1,1,1,3,3,3,4,4,
             4,5,5,5,6,6,6,6,7,7,];

var obj = _.frequencies(array);
console.log("Original Array : ", array);
console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Original Array :  [
  1, 1, 1, 1, 1, 1, 3,
  3, 3, 4, 4, 4, 5, 5,
  5, 6, 6, 6, 6, 7, 7
]
Generated Mapping Object:  { '1': 6, '3': 3, '4': 
3, '5': 3, '6': 4, '7': 2 }

```