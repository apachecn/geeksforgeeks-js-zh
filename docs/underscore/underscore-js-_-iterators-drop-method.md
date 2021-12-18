# 下划线. _ .iterators.drop()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-drop-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-drop-method/)

借助 **_.iterators.drop()** 方法，我们可以在调用迭代器时获取值，但会将值降至 **numberToDrop** 值，并使用该方法返回生成的值。

**语法:**

```
_.iterators.drop(iter, numberToDrop)
```

**返回:**在删除某些值后，通过迭代器返回这些值。

**例 1:**

在这个方法中，我们可以看到，通过使用 **_.iterators.drop()** 方法，我们可以在每次调用迭代器时获取值，但是会丢弃一些值，直到 **numberToDrop** 值。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geeks", "for", "Geeks"]);

var geek = _.iterators.drop(iter, 2);

geek();
```

**输出:**

```
'Geeks'
```

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["E", "D", "C", "B", "A"]);

var geek = _.iterators.drop(iter, 2);

geek();
geek();
geek();
```

**输出:**

```
'C'
'B'
'A'

```