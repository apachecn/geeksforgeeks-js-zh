# 洛达什 _。存取器()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-accessor-method/](https://www.geeksforgeeks.org/lodash-_-accessor-method/)

**洛达什 _。accessor()方法**返回一个函数，该函数将尝试在给定对象中查找给定字段。

**语法:**

```
_.accessor( field_name );

```

**参数:**该方法取上述单参数，描述如下:

*   **Field _ name:** This method takes the field to be searched in a given object.

**返回值:**该方法返回一个函数，该函数将尝试在给定对象中查找给定字段。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## Javascript

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var ob = { gfg : "GeeksforGeeks" } 
var gfgg = _.accessor('gfg'); 

console.log(gfgg(ob));
```

**输出:**

```
GeeksforGeeks

```

**例二:**

## Javascript

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var ob = { gfg : "GeeksforGeeks" } 
var gfgg = _.accessor('geeks'); 

console.log(gfgg(ob));
```

**输出:**

```
undefined

```