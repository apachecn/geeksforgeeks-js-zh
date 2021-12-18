# 洛达什 _。inc()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-inc-method/](https://www.geeksforgeeks.org/lodash-_-inc-method/)

**洛达什 _。inc()方法**通过给定值加 1 返回结果。

**语法:**

```
_.inc( value );

```

**参数:**该方法取一个值，用 _。inc()方法。

**返回值:**该方法通过给定值加 1 返回结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var val = 100 
var incrVal  = _.inc( val ); 

console.log("The Given value is :", val); 
console.log("The Increment of Given value is :", incrVal);
```

**输出:**

```
The Given value is : 100
The Increment of Given value is : 101

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var val = 51 
var incrVal  = _.inc( val ); 

console.log("The Given value is :",val); 
console.log("The Increment of Given value is :",incrVal);
```

**输出:**

```
The Given value is : 51
The Increment of Given value is : 52

```