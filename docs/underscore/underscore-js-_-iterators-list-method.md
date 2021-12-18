# 下划线. js _ 迭代器.列表()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-列表-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-list-method/)

借助 **_.iterators.List()** 方法，我们可以得到迭代器，当调用该迭代器时，使用该方法给出 List 的下一个值。

**语法:**

```
_.iterators.List(array:Array)

```

**参数值:**该方法接受如上所述的单个参数，如下所述:

*   **Array:** Save the array to which this method will be applied.

**返回:**返回列表的迭代器。

**示例 1:** 在这个示例中，我们可以看到，通过使用**_ . iterators . List(Array:Array)**方法，我们能够获得每次调用迭代器时调用的迭代器，并在调用时返回 List 的值。

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var gfg = _.iterators.List(["Geeks", "for", "Geeks"]);

for(var i = 0; i < 3; i++) {
    console.log(gfg());
}
```

**输出:**

```
Geeks
for
Geeks

```

**例二:**

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var gfg = _.iterators.List(["A", "B", "C", "D", "E"]);

for(var i = 0; i < 3; i++) {
    console.log(gfg());
}
```

**输出:**

```
A
B
C
D
E

```