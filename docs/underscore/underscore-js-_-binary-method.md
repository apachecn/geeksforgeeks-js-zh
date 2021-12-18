# 下划线. js _。二进制()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-二进制-方法/](https://www.geeksforgeeks.org/underscore-js-_-binary-method/)

下划线 **_。binary()** 方法 r 返回一个新函数，该函数只接受两个参数，并将这些参数传递给给定函数。其他参数将被丢弃。

**语法:**

```
_.binary( fun )

```

**参数:**该方法采用如上所列的单个参数，讨论如下。

*   **乐趣:**这是给定的功能。

**返回值:**返回一个新函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装**下划线-contrib** 库，并执行以下命令。

```
npm install underscore-contrib

```

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(){
    var mul = 1;
     for (var i = 0; i < arguments.length; i++) {
         mul = mul * arguments[i];
     }
     return mul;
}

var gfgFunc = _.binary(fun);

console.log("Multiplication is :",
        gfgFunc(2,3));
```

**输出:**

```
Multiplication is : 6

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun() {
    var mul = 1;
     for (var i = 0; i < arguments.length; i++) {
         mul = mul * arguments[i];
     }
     return mul;
}

var gfgFunc = _.binary(fun);

// Only operates for first two parameters
console.log("Multiplication is :", 
        gfgFunc(2,23,2,2));
```

**输出:**

```
Multiplication is : 46

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun() {
    return arguments;
}

var gfgFunc = _.binary(fun);

// Only first two parameters will
// be used as arguments
console.log("Binary Arguments are :",
    gfgFunc("a", "b", "c", "d", "e"));
```

**输出:**

```
Binary Arguments are : [Arguments] { '0': 'a', '1': 'b' }

```