# D3.js 最大()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-greatest-method/](https://www.geeksforgeeks.org/d3-js-greatest-method/)

借助**D3 . maximum()**方法，我们可以用这种方法从一个数组中的数字序列中得到最大值。

**语法:**

```
d3.greatest(iterable)

```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**返回最大值。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3

```

**例 1:** 在本例中，我们可以看到，通过使用**D3 . maximum()**方法，我们能够通过使用该方法从数组的序列中获得最大值。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.greatest([5, 4, 3, 2, 1])

console.log(gfg)
```

**输出:**

```
5

```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var gfg = d3.greatest(arr)

console.log(gfg)
```

**输出:**

```
4
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md