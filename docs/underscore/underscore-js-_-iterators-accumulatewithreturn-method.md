# 下划线. js _ iterators . accumulatewitthread()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-accumulatewitthrow-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-accumulatewithreturn-method/)

借助**_ . iterators . accumulatewitthread()**方法，当调用迭代器函数时，我们可以期望在一个数组中返回两个值，当前迭代的输出通过使用该方法传递给下一个迭代值。

**语法:**

```
_.iterators.accumulateWithReturn(iter, binaryFn, initial)
```

**返回:**将数组中的两个值返回给迭代器。

**例 1:**

在这个例子中，我们可以看到，通过使用**_ . iterators . accumulatewithreeturn()**方法，每当我们调用迭代器时，我们都能够在数组中预期这两个值。它总是将当前迭代的结果传递给下一个迭代。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["Geeks", "for", "Geeks"]);

function calculateLength(geeky, element) {
    return [element.length, 'Length of '+element+'is '+element.length];
}

var gfg = _.iterators.accumulate(iter, calculateLength, 0);

for(var i = 0; i < 3; i++) {
    console.log(gfg());
}
```

**输出:**

> [ 5，“极客的长度是 5”]
> 
> [ 3，'的长度为 3 '
> 
> [ 5，“极客的长度是 5”]

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["A", "ABA", "ABCBA", "ABA", "A"]);

function calculateLength(geeky, element) {
    return [element.length, 'Length of '+element+'is '+element.length];
}

var gfg = _.iterators.accumulate(iter, calculateLength, 0);

for(var i = 0; i < 5; i++) {
    console.log(gfg());
}
```

**输出:**

> [ 1，' A 的长度为 1' ]
> 
> [ 3，‘脱落酸长度为 3’]
> 
> [ 5，ABCBA 的长度是 5’]
> 
> [ 3，‘脱落酸长度为 3’]
> 
> [ 1，' A 的长度为 1' ]