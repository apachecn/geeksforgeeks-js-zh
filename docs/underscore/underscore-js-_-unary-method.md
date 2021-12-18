# 下划线. js _。一元()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-unary-method/](https://www.geeksforgeeks.org/underscore-js-_-unary-method/)

下划线 **_。一元()**方法 re 转换一个新函数，该函数只接受一个参数，并将该参数传递给给定函数。其他参数将被丢弃。

**语法:**

```
_.unary( fun )

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

// Making unary function
var gfgFunc = _.unary(fun);

console.log("Arguments are :", 
    gfgFunc(1, 2, 3));
```

**输出:**

```
Arguments are : [Arguments] { '0': 1 }

```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun() {
    return arguments;
}

// Making unary function
var gfgFunc = _.unary(fun);

// Rest arguments are excluded
console.log("Arguments are :", 
    gfgFunc(1, 2, 3, 4, 5, 6, 7, 8));
```

**输出:**

```
Arguments are : [Arguments] { '0': 1 }
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function fun(a){
    return a;
}

// Making unary function
var gfgFunc = _.unary(fun);

// Only one argument is passed
console.log("Best Platform :", 
    gfgFunc("GeeksforGeeks"));
```

**输出:**

```
Best Platform : GeeksforGeeks
```