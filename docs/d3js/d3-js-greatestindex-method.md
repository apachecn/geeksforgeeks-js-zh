# D3.js greatestIndex()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-greatestindex-method/](https://www.geeksforgeeks.org/d3-js-greatestindex-method/)

借助 **d3.greatestIndex()** 方法，我们可以利用这种方法从一个数组中的数字序列中得到最大值的索引。

**语法:**

```
d3.greatestIndex( iterable, accessor )
```

**返回值:**返回最大值的索引。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3
```

**示例 1:** 在这个示例中，我们可以看到，通过使用**D3 . greateestindex()**方法，我们能够使用该方法从数组中获取序列中最大值的索引。

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var greatest_index =
  d3.greatestIndex([5, 4, 3, 2, 1]);

console.log(greatest_index);
```

**输出:**

```
0
```

**例二:**

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var greatest_index =
  d3.greatestIndex([1.5, .44, 3.1, 2.12, 1.01]);

console.log(greatest_index);
```

**输出:**

```
2
```