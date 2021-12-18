# 洛达什 _。xorWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-xorwith-method/](https://www.geeksforgeeks.org/lodash-_-xorwith-method/)

_。xorWith()方法类似于 _。xor()方法，除了它接受被调用来比较数组元素的比较器。结果值的顺序，由它们在数组中出现的顺序决定。

**语法:**

```
_.xorWith([arrays], [comparator])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **[array]:** This parameter stores the array to be checked.
*   **[Comparator] (function):** This parameter holds the comparator called by each element and is called with two parameters (arrVal and othVal).

**返回值:**此方法用于返回新的过滤值数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var objects = [{ 'x': 3, 'y': 4 }, { 'x': 4, 'y': 3 }];
var others = [{ 'x': 3, 'y': 3 }, { 'x': 3, 'y': 4 }];

// Use of _.xorWith() 
// method

let gfg = _.xorWith(objects, others, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{ x: 4, y: 3 }, { x: 3, y: 3 }]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var objects = ([ 23, 34, 98 ], [ 34, 23 ]);
var obj = ([ 4, 6 ], [4, 34, 6, 98 ]);

// Use of _.xorWith() 
// method

let gfg = _.xorWith(objects, obj, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 23, 4, 6, 98 ]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var obj1 = ([ 'p', 'q', 'r' ], [ 'u', 's', 't', 'u' ]);

var obj2 = ([ 'p', 'q', 'u', 's' ], [ 't', 'r', 'u' ]);

// Use of _.xorWith() method

let gfg = _.xorWith(obj1, obj2, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 's', 'r' ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。