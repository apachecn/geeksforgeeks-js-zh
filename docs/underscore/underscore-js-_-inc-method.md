# 下划线. js _。inc()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-inc-method/](https://www.geeksforgeeks.org/underscore-js-_-inc-method/)

_。 **inc** ()方法 r 通过将给定值增加 1 来返回结果。

**语法:**

```
_.inc( value );

```

**参数:**该方法取值并递增。

**返回值:**此方法 r 通过给定值增加 1 来返回结果。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var val = 100
var incrVal  = _.inc( val );

console.log("The Given value is :",val);
console.log("The Increment of Given value is :",incrVal);
```

**输出:**

```
The Given value is : 100
The Increment of Given value is : 101

```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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