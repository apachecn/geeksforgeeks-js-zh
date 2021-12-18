# 下划线. js _。isInteger()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isinteger-method/](https://www.geeksforgeeks.org/underscore-js-_-isinteger-method/)

The _。 **是整数** ()方法检查给定值是否为整数值，并返回对应的布尔值。

**语法:**

```
_.isInteger( value );
```

**参数:**

*   **值:**要检查整数值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为整数，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Integer : "
    + _.isInteger(-4)); 
```

**输出:**

```
The Value is Integer : true
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Integer : " 
    + _.isInteger(4.2)); 
```

**输出:**

```
The Value is Integer : false
```

**示例 3:** 对于此方法，值 4.0 和 4 都将被视为整数，因此此方法将返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Integer : " 
    + _.isInteger(4.0));
```

**输出:**

```
The Value is Integer : true
```

**示例 4:** 包含整数值的字符串将返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Integer : " 
    + _.isInteger("4"));
```

**输出:**

```
The Value is Integer : true
```