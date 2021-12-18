# 下划线. js _。bitwiseRight()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-bitwiseright-method/](https://www.geeksforgeeks.org/underscore-js-_-bitwiseright-method/)

_。 **bitwiseRight** ()方法 r 对所有参数使用> >运算符的结果。

**语法:**

```
_.bitwiseRight(val1, val2,..., valn);

```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 返回在参数上使用> >运算符的结果。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bR  = _.bitwiseRight( 1, 3 );

console.log("The bitwiseRight is :", bR);
```

**输出:**

```
The bitwiseRight is : 0

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bR  = _.bitwiseRight( 3, 1 );

console.log("The bitwiseRight is :", bR);
```

**输出:**

```
The bitwiseRight is : 1

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bR  = _.bitwiseRight( 1 );

console.log("The bitwiseRight is :", bR);
```

**输出:**

```
The bitwiseRight is : 1

```