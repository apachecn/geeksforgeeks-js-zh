# D3.js 洗牌机()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-shuffler-method/](https://www.geeksforgeeks.org/d3-js-shuffler-method/)

借助 **d3.shuffler()** 方法，我们可以得到 shuffle 的随机函数，利用这种方法可以对一个数组的随机值进行 shuffle。

**语法:**

```
d3.shuffler( random )
```

**返回值:**返回随机洗牌功能。

**注意:**要执行以下示例，您必须使用此命令提示符安装 d3 库，我们必须执行以下命令。

```
npm install d3
```

**示例 1:** 在这个示例中，我们可以看到，通过使用 **d3.shuffler()** 方法，我们能够获得随机 shuffle 函数，我们可以使用它来使用该方法对数组中的元素进行 shuffle。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

const random = d3.randomLcg(0.67019185816);
var gfg = d3.shuffler(random);

console.log(gfg([0, 1, 2, 3, 4]));
```

**输出:**

```
[ 3, 0, 4, 2, 1 ]
```

**例 2:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

const random = d3.randomLcg(0.5816);
var gfg = d3.shuffler(random);

console.log(gfg([5, 6, -1, 3, 4]));
```

**输出:**

```
[3, 5, 6, -1, 4]
```

**例 3:**

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

for(var i = 0.1; i <= 0.5; i+=0.1) {
    var random = d3.randomLcg(i);
    var gfg = d3.shuffler(random);

    console.log(gfg([-5, 6, -1, 3, -4]));
}
```

**输出:**

```
[ -4, 6, -5, -1, 3 ]
[ -1, 3, -5, -4, 6 ]
[ -5, -4, 6, -1, 3 ]
[ -1, 3, -4, -5, 6 ]
[ 6, -1, -5, -4, 3 ]

```