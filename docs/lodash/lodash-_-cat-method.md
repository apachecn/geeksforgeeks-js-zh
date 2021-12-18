# 洛达什 _。cat()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-cat-method/](https://www.geeksforgeeks.org/lodash-_-cat-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。cat()** **方法**用于将零个或多个参数连接成一个数组。它可以用来连接多种类型的参数，

**语法:**

```
_.cat( arg1, arg2, ..., argn )

```

**参数:**

*   **参数:**这个方法接受多个参数来连接成一个数组。

**返回值:**这个方法返回一个串联数组。

**注意:** 这个方法在正常的 JavaScript 中无法工作，因为它需要安装 Lodash contrib 库。l odash- contrib 库可以使用 **npm 安装 lodash-contrib–保存**来安装

**示例 1:** 在本例中，我们将连接 2 个数组。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Array1
var arr1 = [1,2,3];

// Array2
var arr2 = [4,5,6];

// Concatenation
var arr = _.cat(arr1, arr2); 

console.log("array 1 : " + arr1); 
console.log("array 2 : " + arr2); 
console.log("concatenated array : " + arr);
```

**输出:**

```
array 1 : 1,2,3
array 2 : 4,5,6
concatenated array : 1,2,3,4,5,6

```

**示例 2:** 在本例中，我们将连接 2 个数字形成一个数组。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Number 1
var num1 = 1;

// Number 2
var num2 = 4;

// Concatenation
var arr = _.cat(num1, num2); 
console.log("num1 : " + num1); 
console.log("num2 : " + num2); 
console.log("Concatenated array : " + arr);
```

**输出:**

```
num1 : 1
num2 : 4
Concatenated array : 1,4

```

**示例 3:** 在本例中，我们将连接 3 个数组。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Array1
var arr1 = [1,2,3];

// Array2
var arr2 = [4,5,6];

// Array3
var arr3 = [7,8,9];

// Concatenation
var arr = _.cat(arr1, arr2, arr3); 
console.log("array 1 : " + arr1); 
console.log("array 2 : " + arr2); 
console.log("array 3 : " + arr3);
console.log("Concatenated array : " + arr);
```

**输出:**

```
array 1 : 1,2,3
array 2 : 4,5,6
array 3 : 7,8,9
Concatenated array : 1,2,3,4,5,6,7,8,9

```

**例 4:** The _。cat()函数也将像处理数组一样处理 arguments 对象。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function f(){
  return _.cat(arguments, 4,5,6);
}

console.log("Array is : " + f(1,2,3));
```

**输出:**

```
Array is : 1,2,3,4,5,6

```