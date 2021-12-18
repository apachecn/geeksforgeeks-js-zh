# 洛达什 _。固定()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-fix-method/](https://www.geeksforgeeks.org/lodash-_-fix-method/)

洛达什 **_。fix()** 方法 f 基于由值的存在和 _ 占位符定义的参数模板，固定函数的参数。

该函数接受一个参数，该参数在给定值中被 _ 替换。

**语法:**

```
_.fix( fun, [values] )

```

**参数:**该方法采用如上所列的单个参数，讨论如下。

*   **趣味:**这个参数保存给定的函数。
*   **数值:**传递给乐趣的数值。

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
function mul(a, b, c, d){
    return a*b*c*d;
}

// Making curried function
var gfgFunc = _.fix(mul, 1, 2, 3, _);

// 8 is replaced by _ in given values
console.log("Multiplication is :", gfgFunc(8));
```

**输出:**

```
Multiplication is : 48

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function add(a, b, c){
    return a + b + c;
}

// Making fixed function
var gfgFunc = _.fix(add, 1, 2, _);

console.log("Addition is :", gfgFunc(10));
```

**输出:**

```
Addition is : 13

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(str){
    return str;
}

// Making fixed function
var gfgFunc = _.fix(fun, _);

console.log("Coding Platform :",
      gfgFunc("GeeksforGeeks"));
```

**输出:**

```
Coding Platform : GeeksforGeeks

```