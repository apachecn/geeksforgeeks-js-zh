# 下划线. js _ .迭代器. mapcat()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-mapcat-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-mapcat-method/)

借助 **_.iterators.mapcat()** 方法，我们可以得到函数迭代器，当调用该函数迭代器时，返回的值是迭代器内容的扁平化，并利用该方法与一元函数相结合。

**语法:**

```
_.iterators.mapcat(iter, unaryFn)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **iter:** 此参数保存数组的迭代器列表。
*   **一元键:**此参数保存一元功能键。

**返回值:**返回函数迭代器，该迭代器通过与 unaryFn 映射生成值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

下面的例子说明了 JavaScript 中的下划线. _ .iterators.mapcat()方法:

**示例 1:** 在这个示例中，我们可以看到，通过使用 **_.iterators.mapcat()** 方法，我们能够得到函数迭代器，通过使用这个方法，可以在与一元函数映射后生成值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

function generateNumber (x)  {
    return _.iterators.List(_.range(1, x));
}

var treeIter = _.iterators.Tree([2, [3]]);

var geek = _.iterators.mapcat(treeIter, generateNumber);

geek();
geek();
geek();
```

**输出:**

```
1
1
2
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

function generateNumber (x)  {
    return _.iterators.List(_.range(x));
}

var treeIter = _.iterators.Tree([[2, 1], [1, 3]]);

var geek = _.iterators.mapcat(treeIter, generateNumber);

for(var i = 0; i < 5; i++) {
    console.log(geek());
}
```

**输出:**

```
0
1
0
0
0
```