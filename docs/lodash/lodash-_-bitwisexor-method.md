# 洛达什 _。bitwiseXor()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bitwisexor-method/](https://www.geeksforgeeks.org/lodash-_-bitwisexor-method/)

**洛达什 _。bitwiseXor()方法**返回对所有给定参数使用按位 XOR (^)运算符的结果。

**语法:**

```
_.bitwiseXor(val1, val2, ..., valn);

```

**参数:**该方法取 n 个值，按位异或运算。

**返回值:**该方法返回对所有参数使用按位 XOR 运算符(^)的结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bX  = _.bitwiseXor( 1, 2, 3, 4 ); 

console.log("The bitwiseXor is :", bX);
```

**输出:**

```
The bitwiseXor is : 4

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bX  = _.bitwiseXor( 0, 8 ); 

console.log("The bitwiseXor is :", bX);
```

**输出:**

```
The bitwiseXor is : 8

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bX  = _.bitwiseXor( 1 ); 

console.log("The bitwiseXor is :", bX);
```

**输出:**

```
The bitwiseXor is : 1

```