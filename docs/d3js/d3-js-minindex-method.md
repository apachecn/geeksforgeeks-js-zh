# D3.js minIndex()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-minindex-method/](https://www.geeksforgeeks.org/d3-js-minindex-method/)

借助 **d3.minIndex()** 方法，我们可以得到在数字、字符串或日期数组中被发现最小的值的索引。我们可以使用任何一种数组，我们只是用这个方法得到了**索引的最小值**。

**语法:**

```
d3.minIndex( iterable )
```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**返回最小值的指标。

**注意:**要执行下面的例子，你必须安装 **d3** 库通过使用这个命令提示符我们必须执行下面的命令。

```
npm install d3

```

**例 1:** 在本例中，我们可以看到，通过使用**D3 . minidex()**方法，我们能够在用该方法格式化的数字、字符串和日期的数组中找到最小值的索引。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var index = d3.minIndex(arr);

console.log(index);
```

**输出:**

```
0
```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var index = d3.minIndex([new Date(), 
new Date("2020-09-01"), new Date("2020")])

console.log(index)
```

**输出:**

```
2

```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md