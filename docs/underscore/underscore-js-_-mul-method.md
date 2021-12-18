# 下划线. js _。mul()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-mul-method/](https://www.geeksforgeeks.org/underscore-js-_-mul-method/)

**_。mul** ()方法返回所有给定参数的乘积。

**语法:**

```
_.mul( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法返回所有给定参数的乘积。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mulVal  = _.mul( 8, 22, 10 );

console.log("The Product of given values is :", mulVal);
```

**输出:**

```
The Product of given values is : 1760
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mulVal  = _.mul( 8 );

console.log("The Product of given values is :", mulVal);
```

**输出:**

```
The Product of given values is : 8
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mulVal  = _.mul( 0.8, 0.2, 0.9 );

console.log("The Product of given values is :", mulVal);
```

**输出:**

```
The Product of given values is : 0.14400000000000004
```