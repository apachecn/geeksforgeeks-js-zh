# 下划线. js _ .迭代器.展开()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-展开-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-unfold-method/)

借助 **_.iterators.unfold()** 方法，我们可以从迭代函数中获取值，在迭代函数中，每当使用该方法调用函数时，一元函数都应该返回单个值。

**语法:**

```
_.iterators.unfold( seed, unaryFn )
```

**返回值:**返回迭代函数的值。

**注意:**要执行以下示例，您必须使用以下命令安装**下划线-contrib** 库。

```
npm install underscore-contrib
```

**示例 1:** 在这个示例中，我们可以看到，通过使用**_ . iterators . enfold()**方法，我们能够从迭代函数中获取值，其中每当调用函数时，一元函数只返回单个值。

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

function isGFG (val) {
    return val + " for Geeks";
}

var geek = _.iterators.unfold("Geeks", isGFG);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
Geeks
Geeks for Geeks
Geeks for Geeks for Geeks

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

function plusFive (val) {
    return val + 5;
}

var geek = _.iterators.unfold(1, plusFive);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
1
6
11

```