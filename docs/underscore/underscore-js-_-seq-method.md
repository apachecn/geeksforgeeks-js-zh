# 下划线. js _。seq()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-seq-method/](https://www.geeksforgeeks.org/underscore-js-_-seq-method/)

**_。seq()** 方法检查每个参数是否彼此严格相等(===)。因此，相应地返回一个布尔值。

**语法:**

```
_.seq( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var eq  = _.seq( 6, 6, 6 );

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : true
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var eq  = _.seq( "gfg", "gfg", "gfg" );

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : true
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var eq  = _.seq( 1, "1", 1 );

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : false
```

**例 4:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var eq  = _.seq( 1, 12, 1 );

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : false
```