# 下划线. js _ 迭代器. select()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-选择-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-select-method/)

借助 **_.iterators.select()** 方法，当我们使用该方法调用迭代器时，每当我们从一元谓词函数中得到 true 时，我们就可以从迭代函数中得到值。

**语法:**

```
_.iterators.select(iter, unaryPredicateFn)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **iter:** 此参数保存数组的迭代器列表。
*   **unraypredicatefn:**此参数保存 unraypredicatefn 功能键。

**返回值:**从迭代函数中返回值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

**示例 1:** 在这个示例中，我们可以看到，通过使用 **_.iterators.select()** 方法，每当一元谓词函数每次被调用时，我们都能够从迭代函数中获取值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

var iter = _.iterators.List(["ABC", "Geeks", "XYZ",
                             "for", "Geeks"]);

function isGFG (val) {
    if(val == "Geeks") {
        return true;
    } else if (val == "for") {
        return true;
    } else {
        return false;
    }
}

var geek = _.iterators.select(iter, isGFG);

for(var i = 0; i < 5; i++) {
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

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

var iter = _.iterators.List([1, 2, 3, 4, 5, 6, 7]);

function isOdd (val) {
    if(val%2 == 0) {
        return false;
    } else {
        return true;
    }
}

var geek = _.iterators.select(iter, isOdd);

for(var i = 0; i < 7; i++) {
    console.log(geek());
}
```

**输出:**

```
1
3
5
7
```