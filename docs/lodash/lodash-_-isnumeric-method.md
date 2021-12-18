# 洛达什 _。isNumeric()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnumeric-method/](https://www.geeksforgeeks.org/lodash-_-isnumeric-method/)

**洛达什 _。isNumeric()方法**检查给定值是否为数值，并返回相应的布尔值。它可以是包含数值、指数记数法或数字对象等的字符串。

**语法:**

```
_.isNumeric( value );

```

**参数:**该方法取上述单参数，描述如下:

*   **值:**要检查数值的给定值。

**返回值:**如果给定值为数值，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isNumeric() method
console.log("The Value is Numeric : " + _.isNumeric(10000));  

console.log("The Value is Negative : " + _.isNumeric(10.5)); 

console.log("The Value is Negative : " + _.isNumeric('G')); 

console.log("The Value is Negative : " + _.isNumeric('Geeks'));
```

**输出:**

```
The Value is Numeric : true
The Value is Negative : true
The Value is Negative : false
The Value is Negative : false

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isNumeric() method
console.log("The Value is Numeric : " + _.isNumeric([1,10]));  

console.log("The Value is Negative : " + _.isNumeric("500")); 

console.log("The Value is Negative : " + _.isNumeric({})); 

console.log("The Value is Negative : " + _.isNumeric(null));
```

**输出:**

```
The Value is Numeric : false
The Value is Negative : true
The Value is Negative : false
The Value is Negative : false

```