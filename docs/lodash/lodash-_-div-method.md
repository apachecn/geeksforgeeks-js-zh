# 洛达什 _。div()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-div-method/](https://www.geeksforgeeks.org/lodash-_-div-method/)

**洛达什 _。div()方法**执行除法运算，返回所有给定参数的商。

**语法:**

```
_.div( val1, val2,..., valn )

```

**参数:**该方法取 n 个值，进行运算 _。div()方法。

**返回值:**这个方法返回所有给定参数的商。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var divVal  = _.div( 8, 2, 1 ); 

console.log("The Quotient of given values is :", divVal);
```

**输出:**

```
The Quotient of given values is : 4

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var divVal  = _.div( 16, 2, 4, 1 ); 

console.log("The Quotient of given values is :", divVal);
```

**输出:**

```
The Quotient of given values is : 2

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var divVal  = _.div( 1, 2, 4, 1 ); 

console.log("The Quotient of given values is :", divVal);
```

**输出:**

```
The Quotient of given values is : 0.125

```