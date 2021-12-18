# 下划线. js _。循环()法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-cycle-method/](https://www.geeksforgeeks.org/underscore-js-_-cycle-method/)

**_。cycle()方法**取一个整数值和一个数组，然后用它来构建一个数组，该数组包含给定数组中的迭代次数，字符串端到端。

创建的新数组包含给定次数的给定数组。

**语法:**

```
_.cycle(integer, array);
```

**参数:**

*   **整数:**给定数组迭代的次数。
*   **数组:**迭代后形成新数组的数组

**返回值:**这个方法返回一个循环数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–保存**来安装下划线. js contrib 库

**示例:**在本例中，我们将使用此方法简单地创建一个循环数组。

## JavaScript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');
// Integer
var int = 10;
// Array
var arr = [1, 2, 3];
// Constructing cycled array
var c_arr = _.cycle(int, arr);
console.log("cycled array : ");
console.log(c_arr);
```

**输出:**

```
cycled array :
[
  1, 2, 3, 1, 2, 3, 1, 2, 3,
  1, 2, 3, 1, 2, 3, 1, 2, 3,
  1, 2, 3, 1, 2, 3, 1, 2, 3,
  1, 2, 3
]
```