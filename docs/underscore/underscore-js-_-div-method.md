# 下划线. js _。div()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-div-method/](https://www.geeksforgeeks.org/underscore-js-_-div-method/)

_。 **div** ()方法 r 计算所有给定参数的商。

**语法:**

```
_.div( val1, val2,..., valn );

```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 计算所有给定参数的商。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var divVal  = _.div( 8, 2, 1 );

console.log("The Quotient of given values is :",divVal);
```

**输出:**

```
The Quotient of given values is : 4

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var divVal  = _.div( 16, 2, 4, 1 );

console.log("The Quotient of given values is :",divVal);
```

**输出:**

```
The Quotient of given values is : 2

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var divVal  = _.div( 1, 2, 4, 1 );

console.log("The Quotient of given values is :",divVal);
```

**输出:**

```
The Quotient of given values is : 0.125

```