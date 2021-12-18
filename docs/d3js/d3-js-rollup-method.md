# D3.js rollup()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-rollup-method/](https://www.geeksforgeeks.org/d3-js-rollup-method/)

借助 **d3.rollup()** 方法，我们可以从具有键和值的可迭代数据结构中获得简化图。

**语法:**

```
d3.rollup(iterable, reduce, ...keys)

```

**返回值:**将从 iterables 返回缩减地图。

**注意:**要执行以下示例，您必须使用以下命令的命令提示符安装 **d** 3 库。

```
npm install d3

```

**示例 1:** 在本例中，我们可以看到，通过使用 **d3.rollup()** 方法，我们能够从具有键和值的可迭代数据结构中获得简化图。

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

var gfg = d3.rollup(data, g => g.length, d => d.amount);
console.log(gfg);
```

**输出:**

```
Map { '34.0' => 1, '120.11' => 1, '12.01' => 1, '34.05' => 1 }

```

**例 2:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC",   amount: "34.0",   date: "11/12/2019"},
  {name: "DEF",  amount: "120.11", date: "11/02/2020"},
  {name: "MNO", amount: "12.01",  date: "01/04/2020"},
  {name: "DEF", amount: "34.05",  date: "03/04/2020"}
]

var gfg = d3.rollup(data, g => g.length, d => d.name, d => d.date);

console.log(gfg);
```

**输出:**

```
Map {
  'ABC' => Map { '11/12/2019' => 1 },
  'DEF' => Map { '11/02/2020' => 1, '03/04/2020' => 1 },
  'MNO' => Map { '01/04/2020' => 1 } 
  }

```