# 洛达什 _。字典()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-dictionary-method/](https://www.geeksforgeeks.org/lodash-_-dictionary-method/)

**洛达什 _。dictionary()方法**返回一个函数，该函数将尝试查找给定的字段。

**语法:**

```
funct = _.dictionary( object );

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Object:** This method takes the object of the field to be searched.

**返回值:**该方法返回一个函数，该函数将尝试查找给定的字段。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## Javascript

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var ob = { gfg : "GeeksforGeeks" } 
var gfgg = _.dictionary( ob ); 

console.log(gfgg("gfg"));
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
var gfgg = _.dictionary( ob ); 

console.log(gfgg("geek"));
```

**输出:**

```
undefined

```