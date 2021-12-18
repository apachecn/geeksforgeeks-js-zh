# 下划线. js _。功能化()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-functional-method/](https://www.geeksforgeeks.org/underscore-js-_-functionalize-method/)

**_。functionalize()** 方法 t 取一个函数(使用 **这个** 的那个)并将 **这个** 推入参数列表。返回的函数使用其第一个参数作为原始函数的接收者/上下文，其余参数用作原始函数的整个参数列表。

**语法:**

```
_.functionalize( function )
```

**参数:**这个方法取一个使用**这个**的函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中是行不通的，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function get(g) {
    return this[g];
}

var geekFunc = _.functionalize(get);

var geeks = {
    GeeksforGeeks: "Computer Science Portal for Geeks"
};
console.log(geekFunc(geeks, "GeeksforGeeks"))
```

**输出:**

```
Computer Science Portal for Geeks
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function get(g) {
    return this[g];
}

var geekFunc = _.functionalize(get);

var geeks = {
    GeeksforGeeks: 1000000
};
console.log(geekFunc(geeks, "GeeksforGeeks"))
```

**输出:**

```
1000000
```