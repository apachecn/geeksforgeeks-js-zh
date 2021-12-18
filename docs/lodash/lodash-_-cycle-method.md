# 洛达什 _。循环()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-cycle-method/](https://www.geeksforgeeks.org/lodash-_-cycle-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。然后使用 cycle()方法**构建一个新的数组，该数组包含给定数组的给定迭代次数，这些迭代是首尾相连的。因此，创建的新数组包含给定次数的给定数组。

**语法:**

```
_.cycle( integer, array )
```

**参数:**该方法取两个参数，如上图所示，讨论如下:

*   **整数:**是指定给定数组迭代次数的数字。
*   **数组:**是一个迭代的数组，用来做新的数组。

**返回值:**这个方法返回一个新的循环数组。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash-contrib 库。可以使用 **npm 安装 lodash-contrib–保存**来安装 lodash-contrib 库

**例:**

## Javascript

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Integer denoting times to
// cycle through the array
var int = 12;

// Array that has to be cycled
var arr = [1, 2];

// Constructing cycled array
var c_arr = _.cycle(int, arr);

console.log("Cycled array : ");
console.log(c_arr);
```

**输出:**

```
Cycled array :
[
  1, 2, 1, 2, 1, 2, 1, 2,
  1, 2, 1, 2, 1, 2, 1, 2,
  1, 2, 1, 2, 1, 2, 1, 2
]
```