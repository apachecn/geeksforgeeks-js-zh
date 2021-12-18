# 下划线. _ .iterators.numbers()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-数字-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-numbers-method/)

借助 **_.iterators.numbers()** 方法，我们可以从迭代器函数中获取整数值，该整数值将以该方法中给出的参数开始，并在使用该方法调用时逐个递增。

**语法:**

```
_.iterators.numbers(start)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Start:** This parameter stores the starting value.

**返回值:**返回值从给定的参数开始。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

下面的例子展示了 JavaScript 中的下划线. _ .iterators.numbers()方法:

**例 1:** 在这个方法中，我们可以看到，通过使用 **_.iterators.numbers()** 方法，我们能够从迭代器函数中获取整数值，并在每次使用这个方法调用时将该值递增 1。

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var geek = _.iterators.numbers(20);

for(var i = 0; i < 5; i++) {
    console.log(geek());
}
```

**输出:**

```
20
21
22
23
24
```

**例二:**

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var geek = _.iterators.numbers(8);

for(var i = 0; i < 10; i++) {
    console.log(geek());
}
```

**输出:**

```
8
9
10
11
12
13
14
15
16
17
```