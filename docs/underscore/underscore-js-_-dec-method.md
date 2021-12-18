# 下划线. js _。dec()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-dec-method/](https://www.geeksforgeeks.org/underscore-js-_-dec-method/)

_。**12 月**()方法 r 通过将给定值递减 1 来返回结果。

**语法:**

```
_.dec( value );
```

**参数:**该方法取值并递减。

**返回值:**此方法 r 通过给定值减 1 来返回结果。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var val = 33
var decrVal  = _.dec( val );

console.log("The Given value is :", val);
console.log("The Decrement of Given value is :", decrVal);
```

**输出:**

```
The Given value is : 33
The Decrement of Given value is : 32
```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var val = 100
var decrVal  = _.dec( val );

console.log("The Given value is :", val);
console.log("The Decrement of Given value is :", decrVal);
```

**输出:**

```
The Given value is : 100
The Decrement of Given value is : 99
```