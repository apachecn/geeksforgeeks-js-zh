# 下划线. js _。重复()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-repeat-method/](https://www.geeksforgeeks.org/underscore-js-_-repeat-method/)

****_。repeat()方法** 取一个整数和值，创建一个包含给定值给定值整数倍大小的数组。**

****语法:****

```
_.repeat(n, value) 
```

****参数:****

*   ****n:** 给定的整数，表示该值将在数组中出现的次数。**
*   ****值:**要在数组中 n 次的值。**

****返回值:**这个方法返回一个新创建的数组。**

****注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。 可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。****

****示例 1:** 在本例中，我们将使用此方法生成一个重复数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Integer
var integer = 10;

// Value
var value = "GeeksforGeeks";

// Generating Array using Repeat method
var arr =_.repeat(integer, value);
console.log("Integer : ", integer);
console.log("Value : ", value);
console.log("Generated Array : ", arr);
```

****输出:****

```
Integer :  10
Value :  GeeksforGeeks
Generated Array :  [
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks',
  'GeeksforGeeks'
]
```

****例 2:** 值也可以是整数。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Integer
var integer = 10;

// Value
var value = 1;

// Generating Array using Repeat method
var arr =_.repeat(integer, value);
console.log("Integer : ", integer);
console.log("Value : ", value);
console.log("Generated Array : ", arr);
```

****输出:****

```
Integer :  10
Value :  1
Generated Array :  [
  1, 1, 1, 1, 1,
  1, 1, 1, 1, 1
]
```