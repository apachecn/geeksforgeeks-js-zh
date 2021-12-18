# 洛达什 _。unsplat()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unsplat-method/](https://www.geeksforgeeks.org/lodash-_-unsplat-method/)

洛达什 **_。unsplat()** 方法将一个需要数组的函数作为其最后一个**参数，并返回一个功能相同的函数，但使用一系列尾随参数而不是数组。**

****语法:****

```
_.unsplat( function ); 
```

****参数:**该方法接受如上所述的单个参数，讨论如下:**

*   ****函数:**将最后一个参数作为数组的原始函数。**

****注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。**

```
npm install lodash-contrib 
```

**以下示例说明了 Lodash _。JavaScript 中的 unsplat()方法:**

****例 1:****

## **java 描述语言**

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (val, arr) {
    return val+" : "+arr;
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc("a", 10, 20, 30, 40))
```

****输出:****

```
a : 10, 20, 30, 40 
```

****例 2:****

## **java 描述语言**

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (arr) {
    return arr;
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc(100, 200, 300, 400))
```

****输出:****

```
[ 100, 200, 300, 400 ] 
```

****例 3:****

## **java 描述语言**

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function g (val,arr) {
    return arr.join(val);
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc(" : ", "GeeksforGeeks", "Computer Science Portal for Geeks"))
```

****输出:****

```
GeeksforGeeks : Computer Science Portal for Geeks 
```