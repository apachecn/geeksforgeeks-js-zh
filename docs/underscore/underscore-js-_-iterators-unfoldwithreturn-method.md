# 下划线. _ .iterators.unfoldWithReturn()方法

> 原文:[https://www . geeksforgeeks . org/下划线-js-_-迭代器-unfoldwithread-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-unfoldwithreturn-method/)

借助**_ . iterators . unfoldwithreturn()**方法，我们可以从迭代函数中得到两个值，其中每当使用该方法调用函数时，一元函数都应该返回两个值。

**语法:**

```
_.iterators.unfoldWithReturn(seed, unaryFn)
```

**返回值:**从迭代函数返回两个值。

**注意:**要执行以下示例，您必须使用此命令提示符安装**下划线-contrib** 库，并执行以下命令。

```
npm install underscore-contrib
```

**示例 1:** 在这个示例中，我们可以看到，通过使用**_ . iterators . unfoldwithreturn()**方法，我们能够从迭代函数中获取值，其中每当调用迭代函数时，一元函数都会返回两个值。

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

function isGFG (val) {
    return [val, String(val.length)];
}

var geek = _.iterators.unfoldWithReturn("Geeks", isGFG);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
Geeks
[ 'Geeks', '5' ]
[ [ 'Geeks', '5' ], '2' ]

```

**例 2:**

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

function isGFG (val) {
    return [val + 1, val * 5];
}

var geek = _.iterators.unfoldWithReturn(1, isGFG);

for(var i = 0; i < 2; i++) {
    console.log(geek());
}
```

**输出:**

```
1
[ 2, 5 ]

```