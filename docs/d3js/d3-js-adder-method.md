# D3.js 加法器()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-adder-method/](https://www.geeksforgeeks.org/d3-js-adder-method/)

借助 **d3。加法器()**方法，我们可以让加法器计算浮点值的全精度和，用这个方法设置 0 为默认值。

**语法:**

```
const adder = new d3.Adder()
```

**参数:**此功能无参数。

**返回值:**返回加法器计算浮点值的全精度和。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3

```

**例 1:** 在这个例子中，我们可以看到通过使用 **d3。加法器()**方法，利用这种方法可以得到计算浮点数全精度和的加法器。

**文件名:**

```
// Defining d3 variable  
var d3 = require('d3');

const adder = new d3.Adder();
for (let i = 0; i < 3; i++) {
  adder.add(.01);
}

console.log(adder.valueOf());
```

**输出:**

```
0.03
```

**示例 2:** **文件名:**

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = []
for(var i = 0; i < 10; i++) {
    arr.push(i);
}

const adder = new d3.Adder();
for (let i = 0; i < 10; i++) {
  adder.add(arr[i]);
}

console.log(adder.valueOf());
```

**输出:**

```
45
```

**注意:**上述程序将使用以下命令编译运行:

```
node index.js
```

**参考:**T2】https://github.com/d3/d3-array/blob/master/README.md