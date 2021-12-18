# 洛达什 _。isFloat()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isfloat-method/](https://www.geeksforgeeks.org/lodash-_-isfloat-method/)

**洛达什 _。isFloat()方法**检查给定值是否为 Float 值，并返回相应的布尔值。

**语法:**

```
_.isFloat( value );

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**要检查浮点值的给定值。

**返回值:**该方法返回一个布尔值(如果给定值为偶数，则返回真，否则返回假)。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking 
console.log("The Value is Float : " + _.isFloat(5.56));

console.log("The Value is Float : " + _.isFloat(5.0));

console.log("The Value is Float : " + _.isFloat(5));

console.log("The Value is Float : " + _.isFloat(0.5));
```

**输出:**

```
The Value is Float : true
The Value is Float : false
The Value is Float : false
The Value is Float : true

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking 
console.log("The Value is Float : " + _.isFloat(10));

console.log("The Value is Float : " + _.isFloat());

console.log("The Value is Float : " + _.isFloat(23.60));

console.log("The Value is Float : " + _.isFloat(50.08));
```

**输出:**

```
The Value is Float : false
The Value is Float : false
The Value is Float : true
The Value is Float : true

```