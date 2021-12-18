# 下划线. js _ 迭代器. K()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代器-k-method/](https://www.geeksforgeeks.org/underscore-js-_-iterators-k-method/)

借助 **_.iterators.K()** 方法，我们可以得到这个方法调用时从给定值生成一个值的函数。

**语法:**

```
_.iterators.K(value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter keeps a given value.

**返回:**在调用函数时，一次返回一个值。

**注意:**要执行下面的示例，您必须安装**下划线-contrib** 库通过使用此命令提示符，我们必须执行以下命令。

```
npm install underscore-contrib

```

下面的例子说明了 JavaScript 中的下划线迭代器方法:

**示例 1:** 在这个示例中，我们可以看到，通过使用 **_.iterators.K()** 方法，我们能够获得函数，该函数给出了在使用该方法创建迭代器时定义的值。

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var iter = _.iterators.K("Geeks for Geeks");

iter();
```

**输出:**

```
'Geeks for Geeks'
```

**例二:**

## Javascript

```
// Defining underscore contrib variable 
var _ = require('underscore-contrib');

var pi = _.iterators.K(3.141592653589793);

pi();
```

**输出:**

```
3.141592653589793
```