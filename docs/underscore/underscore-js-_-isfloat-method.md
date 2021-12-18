# 下划线. js _。isFloat()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isfloat-method/](https://www.geeksforgeeks.org/underscore-js-_-isfloat-method/)

The _。 **是浮点** ()方法检查给定值是否为浮点值，并返回对应的布尔值。

**语法:**

```
_.isFloat( value );
```

**参数:**

*   **值:**要检查浮点值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为偶数，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Float : " 
    + _.isFloat(4.91));
```

**输出:**

```
The Value is Float : true
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Float : " 
    + _.isFloat(21));
```

**输出:**

```
The Value is Float : false
```

**示例 3:** 对于此方法，值 2.0 和 2 都将被视为整数，因此此方法将返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Float : " 
    + _.isFloat(2.0));
```

**输出:**

```
The Value is Float : false
```

**示例 4:** 包含浮点值的字符串将返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Float : " 
    + _.isFloat("2.188"));
```

**输出:**

```
The Value is Float : true
```