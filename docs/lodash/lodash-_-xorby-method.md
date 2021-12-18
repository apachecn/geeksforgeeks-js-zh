# 洛达什 _。xorBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-xorby-method/](https://www.geeksforgeeks.org/lodash-_-xorby-method/)

_。xorBy 方法类似于 _。xor()方法，除了它接受为每个数组的每个元素调用的迭代，以生成比较它们的标准。结果值的顺序，由它们在数组中出现的顺序决定。

**语法:**

```
_.xorBy(arrays, iteratee)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be checked.
*   **Iteration:** This parameter holds the iteration of each element call and is called with a parameter (value).

**返回值:**这个方法返回新的过滤值数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var x = _.xorBy([3.1, 1.3, 4.6], 
        [3.3, 3.4], Math.floor);
var y = _.xorBy([4.1, 2.3, 7.6], 
        [4.3, 7.4], Math.floor);

// Use of _.xorBy() method
let gfg = _.xorBy(x);
let gfg2 = _.xorBy(y);

// Printing the output 
console.log(gfg);
console.log(gfg2);
```

**输出:**

```
[ 1.3, 4.6 ]
[ 2.3 ]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var x = _.xorBy([{ 'x': 11 }], 
      [{ 'x': 12 }, { 'x': 11 }], 'x');

var y = _.xorBy([{ 'x': 11.2 }], 
      [{ 'x': 12.2 }, { 'x': 56.3 }, 
      { 'x': 38.21 }, { 'x': 11.2 }], 'x');

// Use of _.xorBy() method
// The `_.property` iteratee shorthand

let gfg = _.xorBy(x);
let gfg3 = _.xorBy(y);

// Printing the output 
console.log(gfg);
console.log(gfg3);
```

**输出:**

```
[ { x: 12 } ]
[ { x: 12.2 }, { x: 56.3 }, { x: 38.21 }]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var x = _.xorBy([ 'p'], ['q', 
            'r', 's', 'p' ]);

var y = _.xorBy([ 'tee'], ['tee', 
    'cee', 'dee', 'bee', 'eee' ]);

// Use of _.xorBy() method
// The `_.property` iteratee shorthand

let gfg = _.xorBy(x);
let gfg3 = _.xorBy(y);

// Printing the output 
console.log(gfg);
console.log(gfg3);
```

**输出:**

```
['q', 'r', 's' ]
['cee', 'dee', 'bee', 'eee' ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。