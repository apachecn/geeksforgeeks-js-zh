# 下划线. js _ 迭代器. take()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-take-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-take-method/)

借助 **_.iterators.take()** 方法，我们可以得到从 1 开始到 **numberToTake** 变量的迭代函数的值，并在每次使用该方法调用迭代函数时返回值。

**语法:**

```
_.iterators.take(iter, numberToTake)
```

**返回:**从迭代函数中返回值。

**例 1:**

在这个例子中，我们可以看到，通过使用 **_.iterators.take()** 方法，每当我们调用迭代函数时，我们都可以从迭代函数中获取最大值 **numberToTake** 。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geeks", "for", "Geeks", "ABC", "XYZ"]);

var geek = _.iterators.take(iter, 3);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
Geeks
for
Geeks
```

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List([1, 2, 3, 4, 5, 6]);

var geek = _.iterators.take(iter, 3);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
1
2
3
```