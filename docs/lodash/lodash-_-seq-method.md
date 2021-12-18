# 洛达什 _。seq()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-seq-method/](https://www.geeksforgeeks.org/lodash-_-seq-method/)

**洛达什 _。seq()方法**检查每个参数是否严格相等(===)并返回相应的布尔值。

**语法:**

```
_.seq( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值进行运算 _。seq()方法。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.seq( 6, 6, 6 ); 

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : true
```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.seq( "gfg", "gfg", "gfg" ); 

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : true
```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.seq( 1, "1", 1 ); 

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : false
```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.seq( 1, 12, 1 );

console.log("Each of the arguments is equal to others :", eq);
```

**输出:**

```
Each of the arguments is equal to others : false
```