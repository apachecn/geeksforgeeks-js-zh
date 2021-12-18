# 下划线. js _ 迭代器.切片()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-切片-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-slice-method/)

借助 **_.iterators.slice()** 方法，我们可以从迭代函数中获取值，但它将丢弃由 **numberToDrop** 给出的值的数量，并在使用该函数调用时逐个返回剩余值的最大值 **numberToTake** 。

**语法:**

```
_.iterators.slice(iter, numberToDrop, numberToTake)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **iter:** 此参数保存数组的迭代器列表。
*   **numberToDrop:** 此参数表示要下降的值。
*   **numberToTake:** 此参数是要取的值。

**返回值:**每当调用迭代函数时返回值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

下面的例子说明了一个方法:

**示例 1:** 在这个示例中我们可以看到，通过使用 **_.iterators.slice()** 方法，我们可以从 **numberToDrop** 开始删除一些值后得到值，并使用该方法返回定义为 **numberToTake** 的值的最大数量。

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List([1, 2, 3, 4, 5, 6, 7, 8]);

var geek = _.iterators.slice(iter, 4, 2);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
5
6

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.List(["ABC", "XYZ", "Geeks",
                             "for", "Geeks"]);
var geek = _.iterators.slice(iter, 2, 3);

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