# 洛达什 _。补码()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-complement-method/](https://www.geeksforgeeks.org/lodash-_-complement-method/)

洛达什 **_。complete()**方法返回一个与给定谓词函数的意义相反的函数。

**语法:**

```
_.complement( function );

```

**参数:**该方法接受上面列出并在下面讨论的单个参数。

*   **函数:**定义的包含返回逻辑的参数谓词函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 complement()方法:

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFun (x) {
    return x>=2 ;
}

var comp = _.complement(gfgFun);

var x=1000;

console.log("Without Complement Function:",gfgFun(x))

console.log("With Complement Function:",comp(x));
```

**输出:**

```
Without Complement Function: true
With Complement Function: false

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function gfgFun (x) {
    return x=="Geeks" ;
}

var comp = _.complement(gfgFun);

var x="GeeksforGeeks";
console.log("Without Complement Function:",gfgFun(x))

console.log("With Complement Function:",comp(x));
```

**输出:**

```
Without Complement Function: false
With Complement Function: true

```