# D3.js maxIndex()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-maxindex-method/](https://www.geeksforgeeks.org/d3-js-maxindex-method/)

借助 **d3.maxIndex()** 方法，我们可以得到在数字、字符串或日期数组中被发现最大的值的索引。我们可以使用任何一种数组，我们只是通过使用这种方法得到了最大值的**指数。**

**语法:**

```
d3.maxIndex( iterable )
```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Iterative:** Insert any kind of iterative object.

**返回值:**将返回最大值的索引。

**注意:**要执行下面的例子，你必须安装 d3 库通过使用这个命令提示符我们必须执行下面的命令。

```
npm install d3
```

**示例 1:** 在本例中，我们可以看到，通过使用 **d3.maxIndex()** 方法，我们能够在由该方法格式化的数字、字符串和日期的数组中找到最大值的索引。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var index = d3.maxIndex(arr)

console.log(index)
```

**输出:**

```
4
```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var index = d3.maxIndex([new Date(), 
new Date("2020-09-01"), new Date("2020")])

console.log(index)
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