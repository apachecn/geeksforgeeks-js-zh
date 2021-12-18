# D3.js 平分线左()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-bisector-left-method/](https://www.geeksforgeeks.org/d3-js-bisector-left-method/)

借助**平分线. left()** 方法，我们可以这样插入排序数组中的元素:如果数组中的值等于或大于要插入的元素，那么将使用此方法插入当前元素的左侧。

**语法:**

```
bisector.left(arr, ele)
```

**参数:**该函数有如下参数，如上所述，描述如下:

*   **arr:** is an array passed as a parameter.
*   **ele:** is the value to be inserted.

**返回值:**返回新插入元素的索引。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3
```

**示例 1:** 在这个示例中，我们可以看到，通过使用**等分线. left()** 方法，我们能够获得要插入排序数组左侧的元素的索引。

```
// Defining d3 contrib variable  
var d3 = require('d3');

var bisect = d3.bisector(i => i.int)
var gfg = bisect.left([1, 2, 3, 4, 5], 3)

console.log(gfg)
```

**输出:**

```
0
```

**例 2:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(Math.random());
}

var bisect = d3.bisector(i => i.float)
var gfg = bisect.left(arr, 3)

console.log(gfg)
```

**输出:**

```
0

```