# 下划线. js _。假()法

> 原文:[https://www . geesforgeks . org/下划线-js-_-false-method/](https://www.geeksforgeeks.org/underscore-js-_-falsey-method/)

_。**false**()方法检查给定值是否为 false，相应返回一个布尔值。虚假值是布尔上下文中强制为 **虚假的** 的值。

**语法:**

```
_.falsey( value );
```

**参数:**

*   **值:**要检查给定值的假值。

**返回值:**该方法返回一个**布尔值**(如果给定值为假，则返回真，否则返回假)。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** False 布尔值始终返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.falsey(false);;

console.log("Given Value is Falsey : ",bool);
```

**输出:**

```
Given Value is Falsey : true
```

**示例 2:** 现有值返回真布尔值，因此该方法返回假。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.falsey(10);;

console.log("Given Value is Falsey : ",bool);
```

**输出:**

```
Given Value is Falsey : false    
```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.falsey([ 1, 2, 3 ]);;

console.log("Given Value is Falsey : ",bool);
```

**输出:**

```
Given Value is Falsey : false
```

**例 4:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.falsey(true);;

console.log("Given Value is Falsey : ",bool);
```

**输出:**

```
Given Value is Falsey : false    
```