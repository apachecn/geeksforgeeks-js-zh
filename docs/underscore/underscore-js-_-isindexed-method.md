# 下划线. js _。方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isindexed-method/](https://www.geeksforgeeks.org/underscore-js-_-isindexed-method/)

The _。 **isIndexed()** 方法检查给定值是否可以被认为是“Indexed”，并返回对应的布尔值。索引值是接受数值索引来访问其元素的值。

**语法:**

```
_.isIndexed( value );
```

**参数:**

*   **值:**要检查索引值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值是 Indexed，则返回 true，否则返回 false)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**示例 1:** 数组可以被视为索引值，并且可以使用数字索引来访问其元素。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Indexed : " 
    + _.isIndexed([1, 3, 5]));
```

**输出:**

```
The Value is Indexed : true
```

**示例 2:** 此方法为映射返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Indexed : " 
    + _.isIndexed({1:3, 2:3}));
```

**输出:**

```
The Value is Indexed : false

```

**示例 3:** 对于字符串，此方法返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Indexed : " 
    + _.isIndexed("GeeksforGeeks"));
```

**输出:**

```
The Value is Indexed : true
```