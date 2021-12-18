# 洛达什 _。splat()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-splat-method/](https://www.geeksforgeeks.org/lodash-_-splat-method/)

**_。splat()** 方法接受一个接受一个或多个参数的函数，因此返回一个接受数组并将其元素用作原始函数参数的函数。

**语法:**

```
_.splat( function );

```

**参数:**该方法接受如上所述的单个参数，讨论如下:

*   **函数:**包含参数的原始函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 splat()方法:

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function addNum (a, b) {
    return a + b;
}

var listTwoNamesFromArray = _.splat(addNum);

console.log( listTwoNamesFromArray([1, 10]) );
```

**输出:**

```
11

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function addNum (a, b) {
    return a +" : "+ b;
}

var listTwoNamesFromArray = _.splat(addNum);

console.log( listTwoNamesFromArray(["GeeksforGeeks", 
    "Computer Science Portal for Geeks"]) );
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks

```