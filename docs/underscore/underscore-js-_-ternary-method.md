# 下划线. js _。三元()法

> 原文:[https://www . geesforgeks . org/下划线-js-_-三元-方法/](https://www.geeksforgeeks.org/underscore-js-_-ternary-method/)

下划线 **_。三元()** **方法** r 返回一个新函数，该函数只接受三个参数，并将这些参数传递给给定函数。给出的任何附加参数都将被丢弃。

**语法:**

```
_.ternary( fun )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **乐趣:**这是应该用于参数的功能。

**返回值:**这个方法返回一个新的函数。

**注意:**这个方法在普通的 JavaScript 中无法工作，因为它需要安装**下划线-contrib** 库。可以使用 **npm 安装下划线-contrib** 进行安装

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function to be used
function fun() {
    return arguments;
}

// Making ternary function
var gfgFunc = _.ternary(fun);

console.log("Arguments are :",
    gfgFunc(1, 2, 3));
```

**输出:**

```
Arguments are : [Arguments] { '0': 1, '1': 2, '2': 3 }

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function to be used
function fun() {
    return arguments;
}

// Making the ternary function
var gfgFunc = _.ternary(fun);

// Arguments more than 3 are excluded
console.log("Arguments are :",
    gfgFunc(1, 2, 3, 4, 5, 6, 7, 8));
```

**输出:**

```
Arguments are : [Arguments] { '0': 1, '1': 2, '2': 3 }

```

**示例 3:** 在本例中，我们将添加参数，但只有前 3 个参数将使用此方法。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function to be used
function add() {
    s=0;
    for (i=0; i<3; i++) {
        s+=arguments[i];
    }
    return s;
}

// Making the ternary function
var gfgFunc = _.ternary(add);

// Arguments more than 3 are excluded
console.log("Sum of first 3 arguments is :",
    gfgFunc(1, 2, 3, 4, 5, 6, 7));
```

**输出:**

```
Sum of first 3 arguments is : 6

```