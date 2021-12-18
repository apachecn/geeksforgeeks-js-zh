# 下划线. js _。bitwiseAnd()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-bitwisand-method/](https://www.geeksforgeeks.org/underscore-js-_-bitwiseand-method/)

_。 **bitwiseAnd** ()方法 r 对所有参数使用 Bitwise & 运算符的结果。

**语法:**

```
_.bitwiseAnd( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 对所有参数使用按位 & 运算符。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bA  = _.bitwiseAnd( 1, 3 );

console.log("The bitwiseAnd is :", bA);
```

**输出:**

```
The bitwiseAnd is : 1
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bA  = _.bitwiseAnd( 1, 3, 4, 6 );

console.log("The bitwiseAnd is :", bA);
```

**输出:**

```
The bitwiseAnd is : 0
```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bA  = _.bitwiseAnd( 1 );

console.log("The bitwiseAnd is :", bA);
```

**输出:**

```
The bitwiseAnd is : 1
```