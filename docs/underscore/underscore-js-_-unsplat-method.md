# 下划线. js _。unsplat()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-unsplat-method/](https://www.geeksforgeeks.org/underscore-js-_-unsplat-method/)

**_。unsplat()** 方法 t 将一个需要数组的函数作为其最后一个**参数，并返回一个工作方式相同的函数，但使用一个尾随参数列表代替一个数组。**

****语法:****

```
_.unsplat( function );
```

****参数:****

*   ****函数:**将最后一个参数作为数组的原始函数。**

****返回值:**这个方法 r 返回一个函数。**

****注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。**

**可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。****

****例 1:****

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function g (val, arr) {
    return val + " : " + arr;
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc("a", 1, 2, 3, 4))
```

****输出:****

```
a : 1, 2, 3, 4
```

****例 2:****

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function g (arr) {
    return arr;
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc(1, 2, 3, 4))
```

****输出:****

```
[ 1, 2, 3, 4 ]
```

****例 3:****

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function g (val, arr) {
    return arr.join(val);
}

var gfgFunc = _.unsplat(g);

console.log(gfgFunc(" : ", "GeeksforGeeks", 
      "Computer Science Portal for Geeks"))
```

****输出:****

```
GeeksforGeeks : Computer Science Portal for Geeks
```