# 下划线. js _。咖喱()法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-curry-method/](https://www.geeksforgeeks.org/underscore-js-_-curry-method/)

下划线 **_。curry()** 法 r 练习曲给定功能的 curried 版本。如果相反为真，参数将从右向左处理。

**语法:**

```
_.curry( fun, reverse )

```

**参数:**该方法取两个参数，如上所列，讨论如下。

*   **乐趣:**这是给定的功能。
*   **反转:**为可选参数，决定参数是否反转

**返回值:**返回函数的 curried 版本。

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
function fun(a, b, c, d){
    return a + b + c + d;
}

// Making curried function
var gfgFunc = _.curry(fun);

// Only operates for arguments same
// as the number in function
console.log("Addition is :",
        gfgFunc(2)(23)(2)(3));

// Not adds for less arguments
console.log(gfgFunc(1)(2));
```

**输出:**

```
Addition is : 30
[Function: mustBeUnary]
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b, c) {
    return a * b * c;
}

// Making curried function
var gfgFunc = _.curry(fun);

// Only operates for arguments same
// as the number in function
console.log("Multiplication is :",
        gfgFunc(2)(23)(2));

// Not multiplies for less arguments
console.log(gfgFunc(1)(2));
```

**输出:**

```
Multiplication is : 92
[Function: mustBeUnary]

```

**示例 3:** 参数从右向左处理，反转=真。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b, c){
    return arguments;
}

// Making curried function
var gfgFunc = _.curry(fun,true);

// Only operates for arguments same
// as the number in function
console.log("curried arguments are :",
    gfgFunc("arg1")("arg2")("arg3"));
```

**输出:**参数以相反的顺序存储。

```
curried arguments are : [Arguments] 
    { '0': 'arg3', '1': 'arg2', '2': 'arg1' }

```

**示例 4:** 从左到右处理参数，反转=假。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a, b, c){
    return arguments;
}

// Making curried function
var gfgFunc = _.curry(fun,false);

// Only operates for arguments same
// as the number in function
console.log("curried arguments are :",
    gfgFunc("arg1")("arg2")("arg3"));
```

**输出:**

```
curried arguments are : [Arguments] 
    { '0': 'arg1', '1': 'arg2', '2': 'arg3' }

```