# 下划线. js _。methodize()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-method ze-method/](https://www.geeksforgeeks.org/underscore-js-_-methodize-method/)

**_。method ze()**方法 t 使用一个函数，将第一个参数从参数列表中拉出，进入 **这个** 的位置。返回的函数调用原始函数，其接收者( **这个** )在参数列表前面。

**语法:**

```
_.methodize( function );

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **函数:**包含参数的原始函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFunc (obj) {
    return obj.name + ": " + obj.about;
}

var Geeks = {
    name: "GeeksforGeeks",
    about: "Computer Science Portal for Geeks",
    fun: _.methodize(gfgFunc)
};

console.log(Geeks.fun())
```

**输出:**

```
GeeksforGeeks: Computer Science Portal for Geeks

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function gfgFunc (obj) {
    return "Geeks";
}

fun= _.methodize(gfgFunc)
console.log(fun())
```

**输出:**

```
Geeks

```