# 下划线. js _。补码()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-补语-method/](https://www.geeksforgeeks.org/underscore-js-_-complement-method/)

**_。complete()**方法返回一个与给定谓词函数的意义相反的函数。

**语法:**

```
_.complement( function );
```

**参数:**

*   **函数:**包含返回逻辑的谓词函数。

**返回值:**这个方法返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFun (x) {
    return x>=2 ;
}

var comp = _.complement(gfgFun);

var x=3;

console.log("Without Complement Function:", gfgFun(x))

console.log("With Complement Function:", comp(x));
```

**输出:**

```
Without Complement Function: true
With Complement Function: false
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFun (x) {
    return x=="Geeks" ;
}

var comp = _.complement(gfgFun);

var x="Geek";
console.log("Without Complement Function:", gfgFun(x))

console.log("With Complement Function:", comp(x));
```

**输出:**

```
Without Complement Function: false
With Complement Function: true
```