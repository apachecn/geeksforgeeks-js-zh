# 洛达什 _。样品()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sample-method/](https://www.geeksforgeeks.org/lodash-_-sample-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。sample()方法将从集合中提供一个随机元素。

**语法:**

```
_.sample(collection)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **采集:**该参数保存待采样的采集。

**返回值:**此方法用于返回随机元素。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array1 = ([ 3, 6, 9, 12 ]);

// Use of _.sample() method
let gfg = _.sample(array1);

// Printing original Array 
console.log("original array1: ", array1)

// Printing the output 
console.log(gfg);
```

**输出:**

```
original array1: [ 3, 6, 9, 12 ]
12

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array1 = ([ 'mon', 'tue', 'wed',
     'thu', 'fri', 'sat', 'sun']);

// Use of _.sample() method
let gfg = _.sample(array1);

// Printing original Array 
console.log("original array1: ", array1)

// Printing the output 
console.log(gfg);
```

**输出:**

```
original array1: [ 'mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun']
mon

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。