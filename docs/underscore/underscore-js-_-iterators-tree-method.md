# 下划线. js _ 迭代器.树()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-树-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-tree-method/)

借助 **_.iterators.Tree()** 方法，我们可以得到迭代器，利用这种方法可以逐个返回树中的每个值，并将输入作为不同维度的数组。

**语法:**

```
_.iterators.Tree( array )
```

**返回值:**返回迭代函数的值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

**例 1:** 在这个例子中，我们可以看到通过使用 **_.iterators.Tree()** 方法。每当调用迭代函数时，我们都能够从树中一个接一个地获取迭代函数的值。

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var geek = _.iterators.Tree(["A", ["C"], ["B", ["D"]]]);

for(var i = 0; i < 5; i++) {
    console.log(geek());
}
```

**输出:**

```
A
C
B
D

```

**例二:**

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var geek = _.iterators.Tree([1, 5, [3], [2, [4]]]);

for(var i = 0; i < 5; i++) {
    console.log(geek());
}
```

**输出:**

```
1
5
3
2
4

```