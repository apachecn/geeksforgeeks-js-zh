# 下划线. js _。管道()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-管道-方法/](https://www.geeksforgeeks.org/underscore-js-_-pipeline-method/)

**_。pipeline()** 方法 t 获取函数列表，作为数组或参数、，并返回一个函数，该函数以某个值作为其参数，并通过该函数中给出的原始函数的管道运行该函数。

**语法:**

```
_.pipeline( func1, func2,..., funcn );

```

**参数:**该方法接受 n 个函数形式的单个参数，因此对给定值进行运算。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 将函数作为参数传递。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function cb (x) 
{ 
    return x * x * x; 
};
function tp (x) 
{ 
    return 3 * x; 
};
function db (x) 
{ 
    return 2 * x; 
};
var func = _.pipeline(cb, tp, db);

console.log(func(5));
```

**输出:**

```
750

```

**示例 2:** 将函数作为数组传递。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function cb (x) 
{ 
    return x * x * x; 
};
function tp (x) 
{ 
    return 3 * x; 
};
function db (x) 
{ 
    return 2 * x; 
};

var func = _.pipeline([tp, cb, db]);

console.log(func(5));
```

**输出:**

```
6750

```