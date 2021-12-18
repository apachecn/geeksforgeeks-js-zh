# 下划线. js _。存取器()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-访问器-方法/](https://www.geeksforgeeks.org/underscore-js-_-accessor-method/)

**_。accessor()** 方法返回一个函数，该函数将尝试在给定对象中查找给定字段。

**语法:**

```
funct = _.accessor( field_name );
```

**参数:**

*   **Field _ name:** This method takes the field to be searched in a given object.

**返回值:**该方法返回一个函数，该函数将尝试在给定对象中查找给定字段。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : "GeeksforGeeks" }
var gfgg = _.accessor('gfg');

console.log(gfgg(ob));
```

**输出:**

```
GeeksforGeeks
```

**示例 2:** 如果这个函数没有找到任何字段，那么它将返回 undefined。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : "GeeksforGeeks" }
var gfgg = _.accessor('geeks');

console.log(gfgg(ob));
```

**输出:**

```
undefined
```