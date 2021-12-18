# D3.js 组()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-group-method/](https://www.geeksforgeeks.org/d3-js-group-method/)

借助 **d3.group()** 方法，我们可以将可迭代数据结构分组到一个映射中，其中键被定义为来自可迭代的元素，值被定义为数组。

**语法:**

```
d3.group( iterable, ...keys )
```

**返回值:**返回以键为元素，以值为数组的映射。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3
```

**例 1:** 在本例中，我们可以看到通过使用 **d3.group()** 方法。我们能够从组 iterable 中获得映射，其中键是一个元素，值是一个数组。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC", amount: "34.0",   date: "11/12/2015"},
  {name: "DEF", amount: "120.11", date: "11/12/2015"},
  {name: "MNO", amount: "12.01",  date: "01/04/2016"},
  {name: "XYZ", amount: "34.05",  date: "01/04/2016"}
]

var grouped_data = d3.group(data, d => d.name)

console.log(grouped_data)
```

**输出:**

> 地图{
> 'ABC' = > [ {姓名:' ABC '，金额:' 34.0 '，日期:' 11/12/2015 ' }]，
> 'DEF' = > [ {姓名:' DEF '，金额:' 120.11 '，日期:' 11/12/2015 ' }]，
> 'MNO' = > [ {姓名:' MNO '，金额:' 12.01 '，日期:' 01/04/2016 ' }，
> ]

**例 2:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC", amount: "34.0",   date: "11/12/2015"},
  {name: "DEF", amount: "120.11", date: "11/12/2015"},
  {name: "MNO", amount: "12.01",  date: "01/04/2016"},
  {name: "XYZ", amount: "34.05",  date: "01/04/2016"}
]

var grouped_data = d3.group(data, 
        d => d.name, d => d.amount)

console.log(grouped_data)
```

**输出:**

```
Map {
  'ABC' => Map { '34.0' => [ [Object] ] },
  'DEF' => Map { '120.11' => [ [Object] ] },
  'MNO' => Map { '12.01' => [ [Object] ] },
  'XYZ' => Map { '34.05' => [ [Object] ] } 
}

```