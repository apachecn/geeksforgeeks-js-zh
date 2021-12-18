# 下划线. js _。绑定()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-bound-method/](https://www.geeksforgeeks.org/underscore-js-_-bound-method/)

**_。bound()** 方法 r 返回一个函数，该函数是一个对象的属性名，绑定到所创建的对象。

**语法:**

```
_.bound( obj, function);
```

**参数:**

*   **obj:** 定义函数的对象。
*   **函数:**定义的包含返回逻辑的函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgObject = {
    name: "GeeksforGeeks",
    detail: "Computer science portal for geeks",
    geekFunc: function() {
        return this.name + ": " + this.detail;
    }
};

var gfgFunction = _.bound(gfgObject, "geekFunc");
console.log(gfgFunction());
```

**输出:**

```
GeeksforGeeks: Computer science portal for geeks
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgObject = {
    one : 1,
    two : 2,
    geekFunc: function() {
        return this.one + " and " + this.two;
    }
};

var gfgFunction = _.bound(gfgObject, "geekFunc");
console.log(gfgFunction());
```

**输出:**

```
1 and 2
```