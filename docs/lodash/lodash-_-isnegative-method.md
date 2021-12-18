# 洛达什 _。isNegative()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnegative-method/](https://www.geeksforgeeks.org/lodash-_-isnegative-method/)

**洛达什 _。isNegative()方法**检查给定值是否为负值，并返回相应的布尔值。

**语法:**

```
_.isNegative( value );

```

**参数:**该方法取上述单个参数，描述如下:

*   **Value:** The given value is negative.

**返回值:**如果给定值为负，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isNegative() method
console.log("The Value is Negative : " + _.isNegative(-500)); 

console.log("The Value is Negative : " + _.isNegative(500)); 

console.log("The Value is Negative : " + _.isNegative('G'));
```

**输出:**

```
The Value is Negative : true
The Value is Negative : false
The Value is Negative : false

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isNegative() method
console.log("The Value is Negative : " + _.isNegative(-10.5)); 

console.log("The Value is Negative : " + _.isNegative(10.5)); 

console.log("The Value is Negative : " + _.isNegative({}));
```

**输出:**

```
The Value is Negative : true
The Value is Negative : false
The Value is Negative : false

```