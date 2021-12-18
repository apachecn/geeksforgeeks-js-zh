# 下划线. _ .iterators.range()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-范围-方法/](https://www.geeksforgeeks.org/underscore-js-_-iterators-range-method/)

借助 **_.iterators.range()** 方法，我们可以得到迭代器函数，该函数给出给定范围内的值，该值被指定为参数，并在使用该方法调用时递增。

**语法:**

```
_.iterators.range(from, to, by)
```

**参数:**此方法接受三个参数，如上所述，如下所述:

*   **From:** This parameter stores the starting value of the range.
*   **to:** This parameter saves the end value of the range.
*   **By:** This parameter keeps the gap value between and within the range.

**返回:**返回给定范围内的值。

**注意:**要执行以下示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib
```

下面的例子说明了 JavaScript 中的下划线. _ .iterators.range()方法:

**示例 1:** 在这个示例中，我们可以看到，通过使用 **_.iterators.range()** 方法，我们能够从每次调用时都给出递增值的迭代器函数中获取值。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

var geek = _.iterators.range(15, Infinity, 5);

for(var i = 0; i < 5; i++) {
    console.log(geek());
}
```

**输出:**

```
15
20
25
30
35...
```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib');

var geek = _.iterators.range(5, Infinity, 2);

for(var i = 0; i < 3; i++) {
    console.log(geek());
}
```

**输出:**

```
5
7
9...
```