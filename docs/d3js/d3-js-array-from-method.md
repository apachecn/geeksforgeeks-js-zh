# D3.js Array.from()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-array-from-method/](https://www.geeksforgeeks.org/d3-js-array-from-method/)

借助 **Array.from()** 方法，我们可以用这个方法把地图转换成数组。

**语法:**

```
Array.from( map )
```

**返回值:**返回不同元素的数组。

**注意:**要执行以下示例，您必须使用命令提示符安装 **d3** 库，我们必须执行以下命令。

```
npm install d3
```

**示例 1:** 在这个示例中，我们可以看到，通过使用 **Array.from()** 方法，我们能够在转换后从地图中获取数组。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC",   amount: "34.0",   date: "11/12/2015"},
  {name: "DEF",  amount: "120.11", date: "11/12/2015"},
  {name: "MNO", amount: "12.01",  date: "01/04/2016"},
  {name: "XYZ", amount: "34.05",  date: "01/04/2016"}
]
var gfg = d3.group(data, d => d.name);

console.log(Array.from(gfg));
```

**输出:**

```
  [ [ 'ABC', [ [Object] ] ],
  [ 'DEF', [ [Object] ] ],
  [ 'MNO', [ [Object] ] ],
  [ 'XYZ', [ [Object] ] ] ]

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
  {name: "XYZ", amount: "34.05",  date: "03/04/2020"}
]

var gfg = d3.group(data, d => d.name, d => d.date);
console.log(Array.from(gfg));
```

**输出:**

```
[ [ 'ABC', Map { '11/12/2019' => [Array] } ],
  [ 'DEF', Map { '11/02/2020' => [Array] } ],
  [ 'MNO', Map { '01/04/2020' => [Array] } ],
  [ 'XYZ', Map { '03/04/2020' => [Array] } ] ]

```