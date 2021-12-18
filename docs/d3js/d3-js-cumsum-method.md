# D3.js cumsum()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-cumsum-method/](https://www.geeksforgeeks.org/d3-js-cumsum-method/)

借助 **d3.cumsum()** 的方法，我们可以得到一个数组所有值的**累计和**，也就是用这种方法，第 I 个索引处的值就是从索引 0 到索引 I 的值的累计和。

**语法:**

```
d3.cumsum( iterable )
```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**返回所有值的累计和。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3
```

**例 1:** 在本例中，我们可以看到，通过使用 **d3.cumsum()** 方法，我们能够使用该方法计算从指数 0 到指数 i <sup>th</sup> 的所有值在指数 i <sup>th</sup> 的累积和。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.cumsum([5, 4, 3, 2, 1])

console.log(gfg)
```

**输出:**

```
Float64Array [ 5, 9, 12, 14, 15 ]

```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var gfg = d3.cumsum(arr)

console.log(gfg)
```

**输出:**

```
Float64Array(5) [ 0, 1, 3, 6, 10 ]

```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2**https://github.com/d3/d3-array/blob/master/README.md**T5】