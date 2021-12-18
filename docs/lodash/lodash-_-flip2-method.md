# Lodash _ flip 2()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flip2-method/](https://www.geeksforgeeks.org/lodash-_-flip2-method/)

Lodash **_.flip2()** 方法返回一个与给定函数的相同的函数，但是以相反的顺序接受前两个参数。所有其余参数的顺序保持不变。

**语法:**

```
_.flip2( function );

```

**参数:**该方法接受如上所述的单个参数，定义如下:

*   **函数:**这个方法取一个带一些参数的函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 JavaScript 中的 Lodash _.flip2()方法:

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFunc(a, b, c) {
    return "a = " + a + 
          ", b = " + b + 
          ", c = " + c;
}

var abc = _.flip2(gfgFunc);

console.log(abc(1, 2, 3));
```

**输出:**

```
a = 2, b = 1, c = 3

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFunc(a, b) {
    return b + " : " + a;
}

var gfg = _.flip2(gfgFunc);

console.log(gfg("GeeksforGeeks", "Computer Science Portal for Geeks"));
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks

```