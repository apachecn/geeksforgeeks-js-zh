# 洛达什 _。紧凑型()功能

> 原文:[https://www.geeksforgeeks.org/lodash-_-compact-function/](https://www.geeksforgeeks.org/lodash-_-compact-function/)

**Lodash** 在处理数组、字符串、对象等时非常有用。它使数学运算和函数范式变得更加容易、简洁。 **_。compact()函数**用于创建一个数组，在 JavaScript 中去掉所有虚假值。

**语法:**

```
_.compact(array)
```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **数组:**是待压缩的数组。

**注意:**值 false、null、0、“”、undefined 和 NaN 是假的。

**返回值:**该函数过滤值后返回数组。

为了更好地理解函数，下面给出了几个例子。

**示例 1:** 将真元素和假元素的列表传递给 _。compact()函数。

## java 描述语言

```
// Requiring the lodash library
let lodash = require("lodash");

// Original array to be compacted
let array = [0, 1, false, 2, '', 3];

let newArray = lodash.compact(array);
console.log("Before compact: " + array);

// Printing newArray 
console.log("After compact: " + newArray);
```

**输出:**

![](img/312b7c741400d04f484d965942e1e2f7.png)

**示例 2:** 将包含所有错误值的列表传递给 _。compact()函数。

## java 描述语言

```
// Requiring the lodash library
let lodash = require("lodash");

// Original array to be compacted
let array = [0, false, '', undefined, NaN];

let newArray = lodash.compact(array);
console.log("Before compact: " + array);

// Printing newArray 
console.log("After compact: " + newArray);
```