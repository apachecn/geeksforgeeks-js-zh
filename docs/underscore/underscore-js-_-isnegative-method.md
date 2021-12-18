# 下划线. js _。isNegative()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isnegative-method/](https://www.geeksforgeeks.org/underscore-js-_-isnegative-method/)

The _。 **为负值** ()方法检查给定值是否为负值，相应返回布尔值。

**语法:**

```
_.isNegative( value );
```

**参数:**

*   **值:**要检查负值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为负，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## java 描述语言

```

// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Negative : " 
    + _.isNegative(-200020)); 
```

**输出:**

```
The Value is Negative : true
```

**例 2:**

## java 描述语言

```

// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Negative : " 
    + _.isNegative(1000000)); 
```

**输出:**

```
The Value is Negative : false
```

**示例 3:** 对于包含负值的字符串，此方法返回 true。

## java 描述语言

```

// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is Negative : " 
    + _.isNegative("-1")); 
```

**输出:**

```
The Value is Negative : true
```