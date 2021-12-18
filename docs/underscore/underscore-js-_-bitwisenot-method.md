# 下划线. js _。bitwiseNot()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-bitwisenot-method/](https://www.geeksforgeeks.org/underscore-js-_-bitwisenot-method/)

_。 **bitwiseNot** ()方法 r 返回在参数上使用~运算符的结果。

**语法:**

```
_.bitwiseNot( value );
```

**参数:**该方法取值对其进行~运算符运算。

**返回值:**这个方法 r 返回在参数上使用~运算符的结果。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bN  = _.bitwiseNot( 1 );

console.log("The bitwiseNot is :", bN);
```

**输出:**

```
The bitwiseNot is : -2
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bN  = _.bitwiseNot( 10 );

console.log("The bitwiseNot is :", bN);
```

**输出:**

```
The bitwiseNot is : -11
```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bN  = _.bitwiseNot( 100 );

console.log("The bitwiseNot is :", bN);
```

**输出:**

```
The bitwiseNot is : -101
```