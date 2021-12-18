# 下划线. js _。fnull()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-fnull-method/](https://www.geeksforgeeks.org/underscore-js-_-fnull-method/)

**_。fnull()** 方法 r 设置一个函数，保护给定的函数不接收不存在的值。当 **fnull()** 功能接收到不存在的值时，返回默认安全值。

**语法:**

```
_.fnull( function, default );

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **函数:**是包含返回逻辑的给定函数。
*   **默认值:**当方法接收到不存在的值时使用的值

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:** 在本例中，当传递 undefined 时，函数返回默认安全值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function func(val) {
    return val;
}

safeVal = _.fnull(func, "GeeksforGeeks");

console.log(safeVal(undefined));
```

**输出:**

```
GeeksforGeeks

```

**例 2:** 当传递现有值时，不使用默认值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function func(val) {
    return val;
}

safeVal = _.fnull(func, "GeeksforGeeks");

console.log(safeVal("GFG"));
```

**输出:**

```
GFG

```

**例 3:** 这个方法也可以用于整数。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function func(val) {
    return val;
}

safeVal = _.fnull(func, 10);

console.log(safeVal(null));
```

**输出:**

```
10

```