# 下划线. _ .rcurry3()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-rcury3-method/](https://www.geeksforgeeks.org/underscore-js-_-rcurry3-method/)

方法 r 是给定函数的简化版本，从右到左最多处理三个参数。

**语法:**

```
_.rcurry3( fun )

```

**参数:**这个方法取上面列出的单个参数，下面讨论:

*   **Fun:** This is a given function passed as a parameter.

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

var curried = _.rcurry3(div);

console.log("Curried division is :", 
    curried(4)(16)(256));
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
function sub(a, b, c) {
    return a-b-c;
}

var curried = _.rcurry3(sub);

console.log("Curried Subtraction is :", 
    curried(2)(4)(200));
```

**输出:**

```
Curried Subtraction is : 194

```

**例 3:** 反方论点是:

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Function
function div(a, b, c) {
    return ("a="+a+" and b="+b+" and c="+c);
}

var curried = _.rcurry3(div);

console.log(curried("a")("b")("c"));
```

**输出:**

```
a=c and b=b and c=a
```