# 下划线. js _。添加()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-add-method/](https://www.geeksforgeeks.org/underscore-js-_-add-method/)

_。**加上**()方法 r 得出所有给定参数的总和。

**语法:**

```
_.add(val1, val2,..., valn);

```

**参数:**该方法返回 n 个值对其进行运算。

**返回值:**这个方法 r 返回所有给定参数的总和。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var sum  = _.add( 1, 2, 4, 1 );

console.log("The Sum is : ", sum);
```

**输出:**

```
The Sum is : 8

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var sum  = _.add( 1 );

console.log("The Sum is : ", sum);
```

**输出:**

```
The Sum is : 1

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var sum  = _.add( 1, 3, 5, 7, 9, 99, 100 );

console.log("The Sum is : ", sum);
```

**输出:**

```
The Sum is : 224

```