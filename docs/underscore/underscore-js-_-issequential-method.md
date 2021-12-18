# 下划线. js _。isSequential()方法

> 原文:[https://www . geeksforgeeks . org/下划线-js-_-issequential-method/](https://www.geeksforgeeks.org/underscore-js-_-issequential-method/)

The _。 **是顺序** ()方法检查给定值是顺序复合类型值还是不是， Exp。数组、参数等。相应地返回一个布尔值。

**语法:**

```
_.isSequential(value);

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**要检查顺序值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值是顺序的，则返回真，否则返回假)。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

下划线. js contrib 库可以使用安装 **npm 安装下划线-contrib-save。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Sequential : " +_.isSequential([1, 2, 3, 4]));
```

**输出:**

```
The Value is Sequential : true

```

**示例 2:** 映射返回假。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Sequential : " +_.isSequential({1:2, 3:4}));
```

**输出:**

```
The Value is Sequential : false

```

**示例 3:** 对于字符串，此方法返回 false

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Sequential : " +_.isSequential("Geeks"));
```

**输出:**

```
The Value is Sequential : false

```