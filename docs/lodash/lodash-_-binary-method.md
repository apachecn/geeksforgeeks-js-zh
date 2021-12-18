# 洛达什 _。二进制()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-binary-method/](https://www.geeksforgeeks.org/lodash-_-binary-method/)

洛达什 **_。binary()** 方法 r 返回一个新函数，该函数只接受两个参数，并将这些参数传递给给定函数。其他参数将被丢弃。

**语法:**

```
_.binary( fun )
```

**参数:**该方法采用如上所列的单个参数，讨论如下。

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
    var mul = 1;
     for (var i = 0; i < arguments.length; i++) {
         mul = mul * arguments[i];
     }
     return mul;
}

var gfgFunc = _.binary(fun);

console.log("Multiplication is :", gfgFunc(2,23));
```

**输出:**

```
Multiplication is : 46

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    var mul = 1;
     for (var i = 0; i < arguments.length; i++) {
         mul = mul * arguments[i];
     }
     return mul;
}

var gfgFunc = _.binary(fun);

// Only operates for first two parameters
console.log("Multiplication is :", gfgFunc(2,23,10));
```

**输出:**

```
Multiplication is : 46

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    return arguments;
}

var gfgFunc = _.binary(fun);

// Only operates for first two parameters
console.log("Arguments are :",
    gfgFunc('arg1', 'arg2', 'arg3', 'arg4'));
```

**输出:**多余的参数被丢弃。

```
Arguments are : [Arguments] { '0': 'arg1', '1': 'arg2' }

```