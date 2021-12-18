# 下划线. js | _。keepIndexed()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-keepindexed-method/](https://www.geeksforgeeks.org/underscore-js-_-keepindexed-method/)

下划线。keepIndexed()方法将一个数组和一个函数作为参数，并返回一个新的数组，该数组由作用于给定数组元素的给定函数的*非空*返回结果填充。

**语法:**

```
_.keepIndexed(array, function)
```

**参数:**

*   **数组:**传递给这个方法的要传递的数组。
*   **函数:**包含生成新数组的条件的函数。

**返回值:**这个方法返回一个新生成的数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 在本例中，我们将通过检查条件来使用此方法生成一个数组。

这里，在函数中，传递数组的索引，该索引进一步用于获取值和比较。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Defining Array
var array = [1, 3, 5, 9]
// Using keepIndexed() Method
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

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Defining Array
var array = [1, 3, 5, 9, 11, 22, 34, 55]
// Using keepIndexed() Method
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

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Defining Array
var array = [1, 3, 5, 9, 11, 22, 34, 55]
// Using keepIndexed() Method
arr = _.keepIndexed(array, function(n) { 
  if(n===4) return array[n];
});

console.log("Generated Array : ");
console.log(arr);
```

**输出:**

```
Generated Array :
[ 11 ]

```