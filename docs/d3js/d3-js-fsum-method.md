# D3.js fsum()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-fsum-method/](https://www.geeksforgeeks.org/d3-js-fsum-method/)

借助 **d3.fsum()** 方法，利用该方法可以得到一个浮点数组值的全精度和，并返回所有值的和。

**语法:**

```
d3.fsum([values])

```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Value:** is an array of values passed as a parameter.

**返回值:**返回数组中值的全精度和。

**注意:**要执行下面的例子，你必须安装 d3 库通过使用这个命令提示符我们必须执行下面的命令。

```
npm install d3

```

**例 1:** 在本例中，我们可以看到，通过使用 **d3.fsum()** 方法，我们能够使用该方法计算数组中浮点值的全精度和。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.fsum([5.4, 4.5, 21.3, -1.9998372, 1.01])

console.log(gfg)
```

**输出:**

```
30.210162800000003

```

**示例 2:** **文件名:**

```
// Defining d3 variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var gfg = d3.fsum(arr)

console.log(gfg)
```

**输出:**

```
10
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md