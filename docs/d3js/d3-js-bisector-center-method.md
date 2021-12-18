# D3.js 平分线.中心()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-bisector-center-method/](https://www.geeksforgeeks.org/d3-js-bisector-center-method/)

借助**平分线. center()** 方法，我们可以将元素 V 插入到一个数组中，这样 V 就可以最接近数组中的第 I 个元素。

**语法:**

```
bisector.center(array, x)

```

**参数:**该函数具有如下参数，如上所述，如下所述:

*   **Array:** It is an array of values passed as a parameter.
*   **x:** is the value to be inserted.

**返回值:**插入新元素后返回数组的索引。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3

```

**示例 1:** 在本例中，我们可以看到，通过使用**平分线. center()** 方法，我们能够插入新元素，使得新元素非常接近使用该方法的数组中的元素。

**文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var bisect = d3.bisector(i => i.int)
var gfg = bisect.center([1, 2, 3, 4, 5], 4)

console.log(gfg)
```

**输出:**

```
0

```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 5; i++) {
    arr.push(i);
}

var bisect = d3.bisector(i => i.float);
var gfg = bisect.center(arr, 4);

console.log(gfg);
```

**输出:**

```
0

```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```