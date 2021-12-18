# 洛达什 _。uniq()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-uniq-method/](https://www.geeksforgeeks.org/lodash-_-uniq-method/)

_。uniq 方法用于从所有给定的数组中按顺序创建唯一值的数组，使用 SameValueZero 进行相等比较。

**语法:**

```
_.union(array)

```

**参数:**该方法接受单个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be checked.

**返回值:**此方法用于返回新的组合值数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let y = ([1, 2, 2, 3, 4, 3, 8, 6]);    

// Use of _.uniq() 
// method

let gfg = _.uniq(y);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 1, 2, 3, 4, 8, 6 ]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let y = (['a', 'b', 'c', 'e', 'd', 'd', 'g', 'i', 'i']);    

// Use of _.uniq() 
// method

let gfg = _.uniq(y);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 'a', 'b', 'c', 'e', 'd', 'g', 'i' ]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let y = (['apple', 'banana', 'banana', 'chikoo',
          'Elderberry', 'Damson 

Date', 'guava', 'Damson Date']);    

// Use of _.uniq() 
// method

let gfg = _.uniq(y);

// Printing the output 
console.log(gfg);
```

**输出:**

```
['apple', 'banana', 'chikoo', 'Elderberry', 'Damson Date', 'guava']

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。