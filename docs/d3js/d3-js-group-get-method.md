# D3.js group.get()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-group-get-method/](https://www.geeksforgeeks.org/d3-js-group-get-method/)

借助 **d3.group.get()** 方法，我们可以从对可迭代数据结构进行分组得到的结果图中获取值。

**语法:**

```
d3.group.get( value )

```

**返回值:**从地图中返回值。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3

```

**示例 1:** 在本例中，我们可以看到，通过使用 **d3.group.get()** 方法，我们能够从从该组获得的结果图中获得值。

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

console.log(grouped_data.get("ABC"))
```

**输出:**

```
[ { name: 'ABC', amount: '34.0', date: '11/12/2015' } ]

```

**例 2:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

data = [
  {name: "ABC", amount: "34.0",   date: "11/12/2019"},
  {name: "DEF", amount: "120.11", date: "11/02/2020"},
  {name: "MNO", amount: "12.01",  date: "01/04/2020"},
  {name: "XYZ", amount: "34.05",  date: "03/04/2020"}
]

var grouped_data = d3.group(data, d => d.name, d => d.date)

console.log(grouped_data.get("XYZ"))
```

**输出:**

```
Map {
  '03/04/2020' => [ 
    { name: 'XYZ', amount: '34.05', date: '03/04/2020' } ]
}

```