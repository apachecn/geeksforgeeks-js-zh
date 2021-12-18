# 下划线. js _。isEven()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-iseven-method/](https://www.geeksforgeeks.org/underscore-js-_-iseven-method/)

The _。 **isEven** ()方法检查给定值是否为偶数，并返回对应的布尔值。

**语法:**

```
_.isEven( value );
```

**参数:**

*   **值:**要检查偶数的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为偶数，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

// Checking
console.log("The Value is Even : " + _.isEven(44));
```

**输出:**

```
The Value is Even : true
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Even : " + _.isEven(21));
```

**输出:**

```
The Value is Even : false
```

**例 3:** 对于值:0，此方法返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Even : " + _.isEven(0));
```

**输出:**

```
The Value is Even : true
```

**例 4:** 对于非整数值，此方法返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Even : " 
    + _.isEven("GeeksforGeeks"));
```

**输出:**

```
The Value is Even : false
```