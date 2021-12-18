# 洛达什 _。减量()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-reductions-method/](https://www.geeksforgeeks.org/lodash-_-reductions-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。reductions()** **方法**用于将元素数组转换为 数组，在该数组中存储折叠操作中的每个中间值。这个方法是同_。方法，只是它返回一个数组。该方法传递一个数组、一个函数、和一个起始值，生成一个新的数组，对和数组进行运算。

**语法:**

```
_.reductions( array, function, start_val )

```

**参数:** 该方法接受三个参数，如上所述，描述如下:

*   **数组:**是要处理的数组。
*   **函数:**是包含迭代条件的函数。
*   **start_val:** 是在开始时传递的值，它在进一步的操作中进一步更新。

**返回值:**这个方法返回一个新数组。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装 Lodash contrib 库。 Lodash contrib 库可以使用**npm 安装 Lodash-contrib–保存**

**示例 1:** 在此示例中，求和数组是以给定的起始值 0 生成的，该值在加法运算时更新。

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Defining the array 
var array = [10, 12, 23, 34, 45]; 

// Using the _.reductions() method
var arr = _.reductions(array, function(st, n) { 
    return st - n; 
}, 0);

console.log("Generated Array : "); 
console.log(arr);
```

**输出:**

```
[ -10, -22, -45, -79, -124 ]

```

**例 2:** 在本例中，通过将的起始值设为 1 来生成乘法数组，该值在进一步乘法时更新。

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Defining the array 
var array = [10, 12, 23, 34, 45]; 

// Using the _.reductions() method
var arr =_.reductions(array, function(st, n) { 
    return st * n; 
}, 1); 

console.log("Generated Array : "); 
console.log(arr);
```

**输出:**

```
Generated Array :
[ 10, 120, 2760, 93840, 4222800 ]

```