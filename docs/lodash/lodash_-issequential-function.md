# 洛达什 _。isSequential()函数

> 原文:[https://www . geeksforgeeks . org/lodash _-is sequential-function/](https://www.geeksforgeeks.org/lodash_-issequential-function/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isSequential()方法**用于检查给定值是否为顺序复合类型值。顺序复合类型的例子是数组和参数。

**语法:**

```
_.isSequential( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**是要检查连续类型值的值。

**返回值:**这个方法返回一个布尔值。如果给定值是顺序类型，则返回 true，否则返回 false。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 **Lodash contrib 库**。**洛达斯贡献库**可以使用 **npm 安装洛达斯贡献**来安装。

**示例 1:** 在此示例中，使用此方法检查数组。

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// Using the _.isSequential() method
console.log("The Value is Sequential : " +
  _.isSequential([2, 4, 6, 8]));
```

**输出:**

```
The Value is Sequential : true

```

**示例 2:** 在本示例中，使用此方法检查具有键值对的对象。

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// Using the _.isSequential() method
console.log("The Value is Sequential : " +
  _.isSequential( {1:5, 5:10} ));
```

**输出:**

```
The Value is Sequential : false

```

**示例 3:** 在本示例中，使用此方法检查字符串。

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// Using the _.isSequential() method
console.log("The Value is Sequential : " +
  _.isSequential("GeeksforGeeks"));
```

**输出:**

```
The Value is Sequential : false

```