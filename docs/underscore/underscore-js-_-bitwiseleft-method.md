# 下划线. js _。bitwiseLeft()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-bitwiseleft-method/](https://www.geeksforgeeks.org/underscore-js-_-bitwiseleft-method/)

_。**bitwiselft**()方法 r 对所有参数使用 < < 运算符的结果。

**语法:**

```
_.bitwiseLeft(val1, val2,..., valn);

```

**参数:**该方法返回 n 个值对其进行运算。

**返回值:**这个方法 r 返回在参数上使用 < < 运算符的结果。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bL  = _.bitwiseLeft( 1, 3 );

console.log("The bitwiseLeft is :", bL);
```

**输出:**

```
The bitwiseLeft is : 8

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bL  = _.bitwiseLeft( 1 );

console.log("The bitwiseLeft is :", bL);
```

**输出:**

```
The bitwiseLeft is : 1

```