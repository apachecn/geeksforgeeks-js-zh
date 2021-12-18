# 下划线. js _ .迭代器.累加()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-累加-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-accumulate-method/)

借助**_ . iterators . aggregate(iter，binaryFn)** 方法，我们可以得到新的迭代器函数，当调用该函数时，它将与 ITER 一起迭代下一步，并使用 binaryFn 生成值。

**语法:**

```
_.iterators.accumulate(iter, binaryFn)
```

**返回:**返回迭代器函数，该函数将使用累积的二元函数生成结果。

**例 1:**

在这个例子中我们可以看到，通过使用**_ . iterators . aggregate(ITER，binaryFn)** 方法，我们能够得到函数迭代器，它将通过使用累加的二进制函数来返回值。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geeks", "for", "Geeks"]);

function calculateLength(geeky, element) {
    return element.length;
}

var gfg = _.iterators.accumulate(iter, calculateLength, 0);

for(var i = 0; i < 3; i++) {
    console.log(gfg());
}
```

**输出:**

> five
> 
> three
> 
> five

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["A", "AB", "ABC", "AB", "A"]);

function calculateLength(geeky, element) {
    return element.length;
}

var gfg = _.iterators.accumulate(iter, calculateLength, 0);

for(var i = 0; i < 5; i++) {
    console.log(gfg());
}
```

**输出:**

> one
> 
> Two
> 
> three
> 
> Two
> 
> one