# 洛达什 _。bitwiseLeft()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bitwiseleft-method/](https://www.geeksforgeeks.org/lodash-_-bitwiseleft-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。bitwiseLeft()方法**用于返回对所有给定参数使用 Bitwise Left 运算符(< <)的结果。

**语法:**

```
_.bitwiseLeft( val1, val2,..., valn )

```

**参数:**该方法采用可变数量的参数，并对其进行按位左操作。

**返回值:**该方法返回对所有参数使用按位左运算符的结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseLeft() method
var bL  = _.bitwiseLeft( 1, 3, 5, 7, 9 ); 

console.log("The bitwiseLeft is :", bL);
```

**输出:**

```
The bitwiseLeft is : 16777216

```

**例 2:**

## java 描述语言

```
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseLeft() method
var bL  = _.bitwiseLeft( 1, 3, 2 );

console.log("The bitwiseLeft is :", bL);
```

**输出:**

```
The bitwiseLeft is : 32

```

**例 3:**

## java 描述语言

```
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseLeft() method
var bL  = _.bitwiseLeft( 1 ); 

console.log("The bitwiseLeft is :", bL);
```

**输出:**

```
The bitwiseLeft is : 1

```