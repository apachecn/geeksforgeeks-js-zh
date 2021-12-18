# 下划线. _ .rcurry2()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-rcury2-method/](https://www.geeksforgeeks.org/underscore-js-_-rcurry2-method/)

下划线. js**_ . rcury2()方法** r 是给定函数的简化版本，其中从右到左最多处理两个参数。

**语法:**

```
_.rcurry2( fun )

```

**参数:**该方法采用上面列出的单个参数，讨论如下:

*   **趣味:**这是作为参数传递的给定函数。

**返回值:**这个方法返回一个 curried 函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装**下划线-contrib** 库，并执行以下命令。

```
npm install underscore-contrib

```

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function div(a, b) {
    return a/b;
}

var curried = _.rcurry2(div);

console.log("Curried division is :", 
    curried(4)(16));
```

**输出:**

```
Curried division is : 4

```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function sub(a, b) {
    return a-b;
}

var curried = _.rcurry2(sub);

console.log("Curried Subtraction is :", 
    curried(2)(4));
```

**输出:**

```
Curried Subtraction is : 2

```

**示例 3:** 如下所示的反向参数:

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function div(a, b) {
    return ("a="+a+" and b="+b);
}

var curried = _.rcurry2(div);

console.log(curried("a")("b"));
```

**输出:**

```
a=b and b=a
```