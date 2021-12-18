# D3.js 最小()法

> 原文:[https://www.geeksforgeeks.org/d3-js-least-method/](https://www.geeksforgeeks.org/d3-js-least-method/)

借助 **d3 .最少()**方法，我们可以用这种方法从数组中的数字序列中得到最少的值。

**语法:**

```
d3.least(iterable)
```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**返回值最小。

**注意:**要执行下面的例子，你必须安装 d3 库通过使用这个命令提示符我们必须执行下面的命令。

```
npm install d3

```

**例 1:** 在本例中，我们可以看到，通过使用 **d3 .最小()**方法，我们能够使用该方法从数组的序列中获得最小的值。

**文件名:**

```
// Defining d3 variable  
var d3 = require('d3');

var gfg = d3.least([5, 4, 3, 2, 1])

console.log(gfg)
```

**输出:**

```
1

```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(Math.random());
}

var gfg = d3.least(arr);

console.log(gfg);
```

**输出:**

```
0.09124116961036877
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md