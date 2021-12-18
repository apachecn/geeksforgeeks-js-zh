# 洛达什 _。绑定()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bound-method/](https://www.geeksforgeeks.org/lodash-_-bound-method/)

洛达什 **_。bound()** 方法返回一个函数，该函数是一个对象的属性名，绑定到所创建的对象。

**语法:**

```
_.bound( obj, function);

```

**参数:**该方法接受两个参数，如上所列，讨论如下。

*   **obj:** 定义函数的对象。
*   **函数:**定义的包含返回逻辑的函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 bound()方法:

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

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
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

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