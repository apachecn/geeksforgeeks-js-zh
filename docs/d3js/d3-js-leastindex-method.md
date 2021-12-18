# D3 . js lestindex()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-leastindex-method/](https://www.geeksforgeeks.org/d3-js-leastindex-method/)

借助**D3 . lestindex()**方法，我们可以用这种方法从数组中的数字序列中得到最小值的索引。

**语法:**

```
d3.leastIndex( iterable )
```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**返回值最小的指标。

**注意:**要执行下面的例子，你必须安装 d3 库通过使用这个命令提示符我们必须执行下面的命令。

```
npm install d3
```

**示例 1:** 在这个示例中，我们可以看到，通过使用**D3 . lestindex()**方法，我们能够使用该方法从数组中获取序列的最小值索引。

**文件名:**

```
// Defining d3 variable  
var d3 = require('d3');

var gfg = d3.leastIndex([42, 12, 34, 21])

console.log(gfg)
```

**输出:**

```
1
```

**示例 2:** **文件名:**

```
// Defining d3 variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i * 2);
}

var gfg = d3.leastIndex(arr)

console.log(gfg)
```

**输出:**

```
0
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md