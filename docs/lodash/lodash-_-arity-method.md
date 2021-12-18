# 洛达什 _。arity()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-arity-method/](https://www.geeksforgeeks.org/lodash-_-arity-method/)

洛达什 **_。arity()** 方法 r 返回一个新函数，该函数相当于给定函数，只是新函数的长度属性等于参数个数。这使得 **而不是** 将函数限制为使用该数量的参数。其唯一的作用是对报道长度的影响。

**语法:**

```
_.arity( numberOfArgs, fun )

```

**参数:**该方法取两个参数，如上所列，讨论如下。

*   **numberOfArgs:** 此参数采用一个数字，表示该方法将采用的参数数量。
*   **乐趣:**这是给定的功能。

**返回值:**返回一个新函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    return "GeeksforGeeks";
}

var gfgFunc = _.arity(4,fun);

console.log("Length of function is :",
    gfgFunc.length);
console.log("Function content :",
    gfgFunc());
```

**输出:**

```
Length of function is : 4
Function content : GeeksforGeeks

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    return arguments[0]*10;
}

var gfgFunc = _.arity(4,fun);

console.log("Length of function is :",
    gfgFunc.length);
console.log("Function content :",
    gfgFunc(10));
```

**输出:**

```
Length of function is : 4
Function content : 100

```