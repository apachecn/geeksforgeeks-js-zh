# 洛达什 _。解压()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unzip-method/](https://www.geeksforgeeks.org/lodash-_-unzip-method/)

_。解压方法类似于 _。zip(即:它创建一个分组元素的数组),除了它接受一个分组元素的数组，并且还创建一个数组，将元素重新分组到它们的预压缩配置。

**语法:**

```
_.unzip(array)

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter holds the array of grouping elements to be processed.

**返回值:**此方法用于返回重组元素的新数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var zipped = _.zip(['a', 'b'], [1, 2], [true, 

false]);    

// Use of _.zip() 
// method
let gfg = _.zip(zipped);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ [['a', 1, true], ['b', 2, false]] ]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var zipped = (['x', 'y'], [5, 6], [true, false]);    

// Use of _.zip() 
// method
let gfg = _.zip(zipped);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ [true, false] ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。