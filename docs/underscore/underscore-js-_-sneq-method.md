# 下划线. js _。sneq()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-sneq-method/](https://www.geeksforgeeks.org/underscore-js-_-sneq-method/)

**_。sneq()** 方法 c 检查每个参数是否与每个严格不相等( === )。因此，相应地返回一个布尔值。

**语法:**

```
_.sneq( val1, val2, ..., valn );

```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var eq  = _.sneq( "2", "2", "2" );

console.log("Each arguments are not "
    + "equal to each other :", eq);
```

**输出:**

```
Each arguments are not equal to each other : false

```