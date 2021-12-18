# D3 . js quantilessorted()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-quantilesorted-method/](https://www.geeksforgeeks.org/d3-js-quantilesorted-method/)

借助**D3 . quantilesreported()**方法，我们可以通过在该方法中使用 p 作为概率来获得给定排序值数组的分位数值。

**语法:**

```
d3.quantileSorted(array, p)

```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Array:** It is an array of values passed as a parameter.
*   **p:** is the range value of quartile.

**返回值:**返回给定排序元素数组的 p 分位数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3

```

**示例 1:** **文件名:index.js**

在这个例子中，我们可以看到通过使用**D3 . quantilesported()**方法，我们能够通过使用这个方法从给定的数组排序值中获得 p 分位数值。

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = [1.21, 1.33, 1.33, 1.34, 1.37, 1.37, 1.38,
1.4, 1.42, 1.43, 1.43, 1.43, 1.44, 1.45, 1.45, 1.45,
1.45, 1.45, 1.45, 1.45]

var gfg = d3.quantileSorted(arr, 0.25)

console.log(gfg)
```

**输出:**

```
1.37
```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 50; i++) {
    arr.push(i);
}

var gfg = d3.quantileSorted(arr, 0.75)

console.log(gfg)
```

**输出:**

```
36.75
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2**https://github.com/d3/d3-array/blob/master/README.md**T5】