# 洛达什 _。unsplatl()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unsplatl-method/](https://www.geeksforgeeks.org/lodash-_-unsplatl-method/)

洛达什 **_。unsplatl()** 方法将一个需要数组的函数作为其**第一个**参数，并返回一个函数，该函数的工作原理相同，但采用一系列前导参数。它类似于 unsplat()方法。它模仿了 ECMAScript 6 中的 rest 参数语法。

**语法:**

```
_.unsplatl( function )

```

**参数:**该方法接受如上所述的单个参数，讨论如下:

*   **函数:**是把第一个自变量作为数组的原始函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (arr, val) {
    return val+" : "+arr;
}

var gfgFunc = _.unsplatl(g);

console.log(gfgFunc(10, 20, 30, 40, "A"))
```

**输出:**

```
A : 10, 20, 30, 40

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (arr) {
    return arr;
}

var gfgFunc = _.unsplatl(g);

console.log(gfgFunc(1, 2, 3, 4))
```

**输出:**

```
[ 1, 2, 3, 4 ]

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (arr,val) {
    return arr.join(val);
}

var gfgFunc = _.unsplatl(g);

console.log(gfgFunc("GeeksforGeeks", "Computer Science Portal for Geeks", " : "))
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks

```