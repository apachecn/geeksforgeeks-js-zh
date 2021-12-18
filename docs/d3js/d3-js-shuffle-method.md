# D3.js shuffle()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-shuffle-method/](https://www.geeksforgeeks.org/d3-js-shuffle-method/)

借助 **d3.shuffle()** 方法，我们可以使用*Fisher–Yates*shuffle 算法从源数组中获取随机洗牌后的数组值，并返回单个数组。

**语法:**

```
d3.shuffle(array[, start[, stop]])

```

**返回值:**返回一个数组，该数组包含来自源数组的值。

**注意:**要执行以下示例，您必须使用以下命令的命令提示符安装 **d3** 库。

```
npm install d3

```

**示例 1:** 在这个示例中，我们可以看到，通过使用 **d3.shuffle()** 方法，我们能够使用 *Fisher-Yates* shuffle 算法从源数组中获取被打乱的数组，并返回单个数组。

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.shuffle([1, 2, 3, 4, 5, 6]);

console.log(gfg);
```

**输出:**

```
[ 1, 5, 6, 3, 4, 2 ]

```

**例二:**

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.shuffle(["A", "B", "C"]);

console.log(gfg);
```

**输出:**

```
[ 'B', 'C', 'A' ]

```