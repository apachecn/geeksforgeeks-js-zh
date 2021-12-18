# 洛达什 _。mul()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mul-method/](https://www.geeksforgeeks.org/lodash-_-mul-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。mul()方法**用于返回所有给定参数的乘积。

**语法:**

```
_.mul( val1, val2, ..., valn )

```

**参数:**该方法取可变数量的值来求积。

**返回值:**这个方法返回所有给定参数的乘积。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 Lodash-contrib–保存**来安装 Lodash contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.mul() method
var mulVal = _.mul( 8, 22, 10 ); 

console.log(
  "The Product of given values is :", mulVal
);
```

**输出:**

```
The Product of given values is : 1760

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.mul() method
var mulVal = _.mul( 8 );

console.log(
  "The Product of given values is :", mulVal
);
```

**输出:**

```
The Product of given values is : 8

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.mul() method
var mulVal = _.mul( 0.8, 0.2, 0.9 );

console.log(
  "The Product of given values is :", mulVal
);
```

**输出:**

```
The Product of given values is : 0.14400000000000004

```