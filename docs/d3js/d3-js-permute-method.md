# D3.js permute()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-permute-method/](https://www.geeksforgeeks.org/d3-js-permute-method/)

借助 **d3.permute()** 方法，我们可以使用指定的键从源对象获取值的数组，并返回一个置换数组的副本。

**语法:**

```
d3.permute(source, keys)
```

**返回值:**返回值的数组。

**注意:**要执行以下示例，您必须使用以下命令的命令提示符安装 **d3** 库。

```
npm install d3
```

**示例 1:** 在本例中，我们可以看到，通过使用 **d3.permute()** 方法，我们能够获得置换后的单个数组，该数组具有源数组中指定的值，并使用键进行置换。

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.permute([1, 2, 3, 4], [3, 2, 1, 0]);

console.log(gfg);
```

**输出:**

```
[ 4, 3, 2, 1 ]
```

**例二:**

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var gfg = d3.permute
(["Geeks", "Geeks", "for"], [0, 2, 1]);

console.log(gfg);
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]
```