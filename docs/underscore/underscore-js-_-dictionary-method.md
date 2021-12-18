# 下划线. js _。字典()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-字典-方法/](https://www.geeksforgeeks.org/underscore-js-_-dictionary-method/)

**_。dictionary()** 方法返回一个函数，该函数将尝试查找给定的字段。

**语法:**

```
funct = _.dictionary( object );
```

**参数:**

*   **Object:** This method takes the object of the field to be searched.

**返回值:**该方法返回一个函数，该函数将尝试查找给定的字段。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : "GeeksforGeeks" }
var gfgg = _.dictionary( ob );

console.log(gfgg("gfg"));
```

**输出:**

```
GeeksforGeeks
```

**示例 2:** 如果这个函数没有找到任何字段，那么它将返回 undefined。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : "GeeksforGeeks" }
var gfgg = _.dictionary( ob );

console.log(gfgg("geek"));
```

**输出:**

```
undefined
```