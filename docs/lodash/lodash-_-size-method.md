# 洛达什 _。尺寸()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-size-method/](https://www.geeksforgeeks.org/lodash-_-size-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。size()方法通过返回数组的长度(如值)或对象自己的可枚举字符串键控属性的数量来获取集合的大小。

**语法:**

```
_.size(collection)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **集合:**此参数保存要检查的集合。

**返回值:**此方法返回集合大小。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array and use _.size() method
var gfg = _.size([12, 14, 36, 29, 10]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
5

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array and use _.size() method
var gfg = _.size({ 'p': 1, 'q': 2, 'r': 5});

// Printing the output 
console.log(gfg);
```

**输出:**

```
3

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array and use _.size() method
var gfg1 = _.size('geeksforgeeks');
var gfg2 = _.size('computer science');

// Printing the output 
console.log(gfg1, gfg2);
```

**输出:**

```
13, 16

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。