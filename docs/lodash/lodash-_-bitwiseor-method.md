# 洛达什 _。bitwiseOr()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bitwiseor-method/](https://www.geeksforgeeks.org/lodash-_-bitwiseor-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。Bitwise OR()方法**用于返回对所有给定参数使用 bitwiseOr 运算符(|)的结果。

**语法:**

```
_.bitwiseOr( val1, val2, ..., valn );

```

**参数:**该方法采用可变数量的参数，并对其进行按位或运算。

**返回值:**该方法返回对所有参数使用按位或运算符的结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseOr() method
var bO = _.bitwiseOr( 1, 2, 3, 4, 5 ); 

console.log("The bitwiseOr is :", bO);
```

**输出:**

```
The bitwiseOr is : 7

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseOr() method
var bO = _.bitwiseOr( 1, 2, 1, 3, 3, 4, 7, 8, 5 ); 

console.log("The bitwiseOr is :", bO);
```

**输出:**

```
The bitwiseOr is : 15

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseOr() method
var bO = _.bitwiseOr( 5 ); 

console.log("The bitwiseOr is :", bO);
```

**输出:**

```
The bitwiseOr is : 5

```