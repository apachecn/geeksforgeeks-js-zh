# 下划线. js _。isJSON()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-isjson-method/](https://www.geeksforgeeks.org/underscore-js-_-isjson-method/)

**_。isJSON()** 方法检查给定值是否为有效的 JSON，并返回对应的布尔值。

**语法:**

```
_.isJSON( value );
```

**参数:**

*   **值:**要检查 JSON 的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值是有效的 JSON，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。下划线. js contrib 库可以使用 **npm 安装下划线-contrib。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is JSON : " +_.isJSON(
'{"GeeksforGeeks" : "A Computer Science portal for Geeks"}'));
```

**输出:**

```
The Value is JSON : true
```

**示例 2:** 对于映射，将返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is JSON : " +_.isJSON(
{GeeksforGeeks : "A Computer Science portal for Geeks"}));
```

**输出:**

```
The Value is JSON : false
```

**例 3:** 对于其他值，此方法返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Checking
console.log("The Value is JSON : " + _.isJSON(["gfg"]));
```

**输出:**

```
The Value is JSON : false
```