# 下划线. js _ .迭代器. foldl()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-foldl-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-foldl-method/)

借助 **_.iterators.foldl()** 方法，我们可以在调用迭代器时从迭代器中获取 single，因为它会通过使用该方法将给定的值归结为一，从而将所有的值转换为一。

**语法:**

```
_.iterators.foldl(iter, binaryFn)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **iter:** 此参数保存数组的迭代器列表。
*   **binaryFn:** 此参数保存二进制功能键。

**返回值:**当我们调用迭代器时返回单个值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用命令提示符我们必须执行以下命令。

```
npm install underscore-contrib

```

下面的例子说明了 JavaScript 中的下划线. _ .iterators.foldl()方法:

**示例 1:** 在这个示例中，我们可以看到，通过使用 **_.iterators.foldl()** 方法，我们能够在调用迭代器时获得返回的单个值，因为它会将给定的值归结为一个。

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geeks", "for", "Geeks"]);

function commaString (a, b) { return a + ", " + b; }

var geek = _.iterators.foldl(iter, commaString);

geek
```

**输出:**

```
'Geeks, for, Geeks'
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["A", "ABA", "ABCBA", "ABA", "A"]);

function spaceString (a, b) { return a + " " + b; }

var geek = _.iterators.foldl(iter, spaceString);

geek
```

**输出:**

```
'A ABA ABCBA ABA A'
```