# 下划线. _ .iterators.map()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-映射-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-map-method/)

借助 **_.iterators.map()** 方法，我们可以得到新迭代器的函数，该函数将通过使用该方法返回使用 List 迭代器值的一元函数的值。

**语法:**

```
_.iterators.map(iter, unaryFn)
```

**返回:**从新迭代器函数中返回值。

在下面给出的例子中，我们只是展示了实现部分，您可以在任何地方使用它。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

**例 1:**

在这个例子中我们可以看到，通过使用 **_.iterators.map()** 方法，我们能够从新的迭代器函数中获取值，该迭代器函数使用一元函数通过使用这个方法生成值。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geek", "for", "Geek"]);

function postfixGeek (val) {
    if(val == "Geek") {
        return val + "s";
    }
    return val;
}

var geek = _.iterators.map(iter, postfixGeek);

geek();
geek();
```

**输出:**

```
'Geeks'
'for'
```

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["A", "ABA", "ABCBA"]);

function postfixLength (val) {
    return val + String(val.length);
}

var geek = _.iterators.map(iter, postfixLength);

geek();
geek();
geek();
```

**输出:**

```
'A1'
'ABA3'
'ABCBA5'
```