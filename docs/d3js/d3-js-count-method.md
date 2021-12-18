# D3.js 计数()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-count-method/](https://www.geeksforgeeks.org/d3-js-count-method/)

借助 **d3.count()** 方法，我们可以得到指定可迭代数据结构中有效值的计数。

**语法:**

```
d3.count(iterable[, accessor])

```

**返回值:**返回有效值的计数。

**注意:**要执行以下示例，您必须使用以下命令的命令提示符安装 **d3** 库。

```
npm install d3

```

**示例 1:** 在本例中，我们可以看到，通过使用 **d3.count()** 方法，我们能够获得指定数据项中有效值的计数。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC",   amount: "34.0",   date: "11/12/2015"},
  {name: "DEF",  amount: "120.11", date: "11/12/2015"},
  {name: "MNO", amount: "12.01",  date: "01/04/2016"},
  {name: "ABC", amount: "34.05",  date: "01/04/2016"}
]

var gfg = d3.count(data, d => d.amount);
console.log(gfg);
```

**输出:**

```
4

```

**例 2:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC",   amount: "34.0",   age: 20},
  {name: "DEF",  amount: "120.11", age: NaN},
  {name: "MNO", amount: "12.01",  age: 23},
  {name: "DEF", amount: "34.05",  age: 24}
]

var gfg = d3.count(data, d => d.age);
console.log(gfg);
```

**输出:**

```
3

```