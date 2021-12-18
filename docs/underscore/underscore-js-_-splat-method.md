# 下划线. js _。splat()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-splat-method/](https://www.geeksforgeeks.org/underscore-js-_-splat-method/)

**_。splat()** 方法接受一个接受一个或多个参数的函数，因此返回一个接受数组并将其元素用作原始函数参数的函数。

**语法:**

```
_.splat( function );
```

**参数:**

*   **Function:** The original function containing independent variables.

**返回值:**这个方法返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function addNum (a, b) {
    return a + b;
}

var listTwoNamesFromArray = _.splat(addNum);

console.log( listTwoNamesFromArray([1, 2]) );
```

**输出:**

```
3
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function addNum (a, b) {
    return a +" : "+ b;
}

var listTwoNamesFromArray = _.splat(addNum);

console.log( listTwoNamesFromArray(
["GeeksforGeeks", "Computer Science Portal for Geeks"]) );
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks
```