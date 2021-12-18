# 洛达什 _。keepindexed()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-keepindexed-method/](https://www.geeksforgeeks.org/lodash-_-keepindexed-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。keepIndexed()方法**将一个数组和一个函数作为参数，并返回一个新的数组，该数组由作用于给定数组元素的给定函数的*非空*返回结果填充。

**语法:**

```
_.keepIndexed( array, function )

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **数组:**这是要传递给这个方法的数组。
*   **函数:**这是包含生成新数组的条件的函数。

**返回值:**这个方法返回一个新生成的数组。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash-contrib 库。可以使用 **npm 安装 lodash-contrib–save 安装 lodash-contrib 库。**

**示例 1:** 在本例中，我们将通过检查条件来使用此方法生成一个数组。数组的索引在函数中传递，该函数进一步用于获取值和进行比较。

## java 描述语言

```
// Defining Lodash-contrib variable 
const _ = require('lodash-contrib'); 

// Defining Array
var array = [1, 3, 5, 9]

// Using the _.keepIndexed() Method
arr = _.keepIndexed(array, function(n) { 
     return array[n] >= 5;
});

console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[ false, false, true, true ]

```

**示例 2:** 在本例中，我们将生成一个充满元素索引的数组。

## java 描述语言

```
// Defining Lodash-contrib variable 
const _ = require('lodash-contrib'); 

// Defining Array
var array = [1, 3, 5, 9, 11, 22, 34, 55]

// Using _.keepIndexed() Method
arr = _.keepIndexed(array, function(n) { 
  return n;
});

console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[
  0, 1, 2, 3,
  4, 5, 6, 7
]

```

**示例 3:** 在本例中，我们将使用 if 条件来获取特定值。

## java 描述语言

```
// Defining Lodash-contrib variable 
const _ = require('lodash-contrib'); 

// Defining Array
var array = [1, 3, 5, 9, 11, 22, 34, 55]

// Using _.keepIndexed() Method
arr = _.keepIndexed(array, function(n) { 
  if(n===5) return array[n];
});

console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[ 22 ]

```