# 下划线. _ .flip2()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-flip2-method/](https://www.geeksforgeeks.org/underscore-js-_-flip2-method/)

**_.flip2()** 方法返回一个与给定的函数相同的函数，但是以相反的顺序接受前两个参数。所有其余参数的顺序保持不变。

**语法:**

```
_.flip2( function );

```

**参数:**这个方法取一个带一些参数的函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFunc(a, b, c) {
    return "Value of a is " +
    a + " and Value of b is " + 
    b + " and Value of c is " + c;
}

var abc = _.flip2(gfgFunc);

console.log(abc(1, 2, 3));
```

**输出:**

```
Value of a is 2 and Value of b is 1 and Value of c is 3

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFunc(a, b) {
    return b + " is " + a;
}

var gfg = _.flip2(gfgFunc);

console.log(gfg("GeeksforGeeks",+
   "Computer Science Portal for Geeks"));
```

**输出:**

```
GeeksforGeeks is Computer Science Portal for Geeks

```