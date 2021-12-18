# 下划线. js _。rCurry()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-rcurry-method/](https://www.geeksforgeeks.org/underscore-js-_-rcurry-method/)

下划线 **_。rCurry()方法** r 返回一个给定函数的 curried 版本，在这里从右到左处理参数。

**语法:**

```
_.rCurry( fun )

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
function div(a, b, c) {
    return a/b/c;
}

var curried = _.rCurry(div);

console.log("Curried division is :", 
    curried(2)(4)(16));
```

**输出:**

```
Curried division is : 2

```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function div(a, b, c, d) {
    return a-b-c-d;
}

var curried = _.rCurry(div);

console.log("Curried Subtraction is :", 
    curried(2)(4)(16)(44));
```

**输出:**

```
Curried Subtraction is : 22

```

**例 3:** 参数颠倒如下:

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function div(a, b, c) {
    return ("a="+a+" and b="+b+" and c="+c);
}

var curried = _.rCurry(div);

console.log(curried("a")("b")("c"));
```

**输出:**

```
a=c and b=b and c=a

```