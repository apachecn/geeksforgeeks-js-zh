# 洛达什 _。isNative()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnative-method/](https://www.geeksforgeeks.org/lodash-_-isnative-method/)

洛达什 **_。isnacional()方法**用于检查指定的值是否是原始的本机函数。

**语法:**

```
_.isNative(value)

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter holds the value to be checked.

**返回值:**如果指定的值是原始的本机函数，则该方法返回布尔值 true，否则返回 false。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Calling _.isNative() functions
console.log(_.isNative("gfg"));
console.log(_.isNative(123));
```

**输出:**

```
false
false

```

**例二:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Calling _.isNative() functions
console.log(_.isNative(Array.prototype.push));
```

**输出:**

```
true

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库。