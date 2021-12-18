# 下划线. js _。sub()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-sub-method/](https://www.geeksforgeeks.org/underscore-js-_-sub-method/)

_。**子**()方法 r 研究所有给定参数的差异。

**语法:**

```
_.sub( val1, val2, ..., valn );

```

**参数:**该方法返回 n 个值对其进行运算。

**返回值:**这个方法 r 返回所有给定参数的差。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var diff  = _.sub( 10, 2, 4, 1 );

console.log("The Difference  is : ", diff);
```

**输出:**

```
The Difference  is :  3

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var diff  = _.sub( 10 );

console.log("The Difference  is : ", diff);
```

**输出:**

```
The Difference  is :  10

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var diff  = _.sub( 1, 3, 5, 7, 9, 99, 100 );

console.log("The Difference  is : ", diff);
```

**输出:**

```
The Difference  is :  -222

```