# 下划线. js _。isInstanceOf()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isinstanceof-method/](https://www.geeksforgeeks.org/underscore-js-_-isinstanceof-method/)

The _。 **isInstanceOf** ()方法检查给定值是否是 a 给定构造函数的实例，并返回对应的布尔值。

**语法:**

```
_.isInstanceOf(value, constructor);
```

**参数:**

*   **Value:** Example of the given value to be checked.
*   **Constructor:** A given constructor.

**返回值:**该方法返回一个**布尔值**(如果给定值是实例，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Instance Of constructor : " 
    + _.isInstanceOf(new Date(),Date));
```

**输出:**

```
The Value is Instance Of constructor : true
```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Instance Of constructor : " 
    + _.isInstanceOf("abc",Date));
```

**输出:**

```
The Value is Instance Of constructor : false
```