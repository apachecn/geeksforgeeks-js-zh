# 下划线. js _。gt()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-gt-method/](https://www.geeksforgeeks.org/underscore-js-_-gt-method/)

_。 **gt()** 方法检查每个参数是否大于其下一个参数。

**语法:**

```
_.gt( val1, val2,..., valn );

```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var greater  = _.gt(4, 1);

console.log(" Each argument is greater than"+
            " its next argument :",greater);
```

**输出:**

```
Each argument is greater than its next argument : true

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var greater  = _.gt(4, 1, 4);

console.log(" Each argument is greater than"+
            " its next argument :",greater);
```

**输出:**

```
Each argument is greater than its next argument: false

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var greater  = _.gt(4, 3, 1);

console.log(" Each argument is greater than"+
            " its next argument :",greater);
```

**输出:**

```
Each argument is greater than its next argument : true

```