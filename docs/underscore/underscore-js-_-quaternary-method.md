# 下划线. js _。四元()法

> 原文:[https://www . geesforgeks . org/下划线-js-_-四元法/](https://www.geeksforgeeks.org/underscore-js-_-quaternary-method/)

下划线 **_。第四纪()** r 返回一个新的函数，该函数只接受四个参数，并将这些参数传递给给定的函数。其他参数将被丢弃。

**语法:**

```
_.quaternary( fun )

```

**参数:**该方法采用上面列出的单个参数，讨论如下:

*   **趣味:**这是作为参数传递的给定函数。

**返回值:**这个方法返回一个新的函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装**下划线-contrib** 库，并执行以下命令。

```
npm install underscore-contrib

```

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun() {
    return arguments;
}

// Making quaternary function
var gfgFunc = _.quaternary(fun);

console.log("Arguments are :", gfgFunc(1, 2, 3, 4));
```

**输出:**

```
Arguments are : [Arguments] { '0': 1, '1': 2, '2': 3, '3': 4 }

```

**示例 2:** 在本例中，我们将添加参数，但只有前 4 个参数将使用此方法。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function add() {
    s = 0
    for(i = 0; i < 4; i++) {
        s += arguments[i]
    }

    return s;
}

// Making quaternary function
var gfgFunc = _.quaternary(add);

// Rest arguments are excluded
console.log("Sum of first 4 arguments is :", 
gfgFunc(1, 2, 3, 4, 5, 6, 7));
```

**输出:**

```
Sum of first 4 arguments is : 10

```