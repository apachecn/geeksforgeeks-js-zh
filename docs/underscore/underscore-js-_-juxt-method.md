# 下划线. js _。juxt()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-juxt-method/](https://www.geeksforgeeks.org/underscore-js-_-juxt-method/)

**_。juxt()** 方法在用给定的参数调用每个函数后，返回一个返回值是结果数组的函数。

**语法:**

```
_.juxt( function1, function2, .., function );
```

**参数:**该方法取 n 个包含逻辑的函数返回值。

**返回值:**这个方法返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

function firstG (val) {
    return val[0];
}
function F(val){
    return val[5];
}
function lastG (val) {
    return val[8];
}

// Defining function
var firstAndLastChars = _.juxt( firstG, F, lastG );

console.log(firstAndLastChars("GeeksforGeeks"));
```

**输出:**

```
[ 'G', 'f', 'G' ]
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

function a() {
    return "a";
}
function b() {
    return "b";
}
function c() {
    return "c";
}
function d() {
    return "d";
}

// Defining function
var firstAndLastChars = _.juxt( a, b, c, d );

console.log(firstAndLastChars("GeeksforGeeks"));
```

**输出:**

```
[ 'a', 'b', 'c', 'd' ]
```