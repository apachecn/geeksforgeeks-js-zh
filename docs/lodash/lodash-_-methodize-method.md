# 洛达什 _。methodize()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-methodize-method/](https://www.geeksforgeeks.org/lodash-_-methodize-method/)

洛达什 **_。method ze()**方法 t 使用一个函数，将第一个参数从参数列表中拉出，进入 **这个** 的位置。返回的函数调用原始函数，其接收器(**)预先挂起参数列表。**

****语法:****

```
_.methodize( function ); 
```

****参数:**该方法接受如上所述的单个参数，如下所述:**

*   ****函数:**包含参数的原始函数。**

****返回值:**这个方法 r 返回一个函数。**

****注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。**

```
npm install lodash-contrib 
```

**以下示例说明了 Lodash _。JavaScript 中的 methodize()方法:**

****例 1:****

## **java 描述语言**

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFunc (obj) {
    return obj.name + " : " + obj.about;
}

var Geeks = {
    name: "GeeksforGeeks",
    about: "Computer Science Portal for Geeks",
    fun: _.methodize(gfgFunc)
};

console.log(Geeks.fun())
```

****输出:****

```
GeeksforGeeks : Computer Science Portal for Geeks 
```

****例 2:****

## **java 描述语言**

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFunc (obj) {
    return "Geeks";
}

fun= _.methodize(gfgFunc)
console.log(fun())
```

****输出:****

```
Geeks 
```