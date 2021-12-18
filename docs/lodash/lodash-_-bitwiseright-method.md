# 洛达什 _。bitwiseRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bitwiseright-method/](https://www.geeksforgeeks.org/lodash-_-bitwiseright-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。bitwiseRight()方法**用于返回对所有给定参数使用 Bitwise Right 运算符(> >)的结果。

**语法:**

```
_.bitwiseRight( val1, val2,..., valn )

```

**参数:**该方法采用可变数量的参数，并对其执行按位右运算符。

**返回值:**该方法返回对所有参数使用按位右运算符(> >)的结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseRight() method
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
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseRight() method
var bR  = _.bitwiseRight( 5, 1 );

console.log("The bitwiseRight is :", bR);
```

**输出:**

```
The bitwiseRight is : 2

```

**例 3:**

## java 描述语言

```
// Adding lodash-contrib library 
var _ = require('lodash-contrib'); 

// Using the _.bitwiseRight() method
var bR  = _.bitwiseRight( 1 ); 

console.log("The bitwiseRight is :", bR);
```

**输出:**

```
The bitwiseRight is : 1

```