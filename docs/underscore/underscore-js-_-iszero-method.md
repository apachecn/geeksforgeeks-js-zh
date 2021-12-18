# 下划线. js _。isZero()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-iszero-method/](https://www.geeksforgeeks.org/underscore-js-_-iszero-method/)

The _。 **为 0**()方法检查给定值是否为 0 值，相应返回布尔值。

**语法:**

```
_.isZero(value);

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**要检查零值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为零，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

下划线. js contrib 库可以使用安装 **npm 安装下划线-contrib-save。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Zero : " +_.isZero(0));
```

**输出:**

```
The Value is Zero : true

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Zero : " +_.isZero(10));
```

**输出:**

```
The Value is Zero : false

```

**示例 3:** 对于包含零的字符串，返回 false

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Zero : " +_.isZero("0"));
```

**输出:**

```
The Value is Zero : false

```