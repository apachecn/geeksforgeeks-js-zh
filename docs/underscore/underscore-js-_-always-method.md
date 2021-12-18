# 下划线. js _。始终()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-总是-方法/](https://www.geeksforgeeks.org/underscore-js-_-always-method/)

**_。始终()**方法 t 取一个值并返回一个函数，该函数将始终返回那个值。

**语法:**

```
_.always( value );
```

**参数:**

*   **Value:** This method takes a value to be returned.

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgFunc = _.always('Geeks');
console.log(gfgFunc());
```

**输出:**

```
Geeks
```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgFunc = _.always(1);
console.log("Value returned is",gfgFunc());
```

**输出:**

```
Value returned is 1
```