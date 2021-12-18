# 洛达什 _。sneq()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sneq-method/](https://www.geeksforgeeks.org/lodash-_-sneq-method/)

**洛达什 _。sneq()方法**检查每个参数是否严格不相等(===)并返回相应的布尔值。

**语法:**

```
_.sneq( val1, val2, ..., valn );

```

**参数:**该方法取 n 个值进行运算 _。sneq()方法。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.sneq( 1, 2, 3 ); 

console.log("Each arguments are not "
    + "equal to each other :", eq);
```

**输出:**

```
Each arguments are not equal to each other : true

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.sneq( 2, 2, 2 );

console.log("Each arguments are not "
    + "equal to each other :", eq);
```

**输出:**

```
Each arguments are not equal to each other : false

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.sneq( "2", 2, 2 );

console.log("Each arguments are not "
    + "equal to each other :", eq);
```

**输出:**

```
Each arguments are not equal to each other : true

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var eq  = _.sneq( "2", "2", "2" );

console.log("Each arguments are not "
    + "equal to each other :", eq);
```

**输出:**

```
Each arguments are not equal to each other : false

```