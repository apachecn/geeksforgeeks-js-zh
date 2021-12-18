# 洛达什 _。不带()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-without-method/](https://www.geeksforgeeks.org/lodash-_-without-method/)

_。方法创建一个过滤形式的新数组，即有值要排除，并给出新值作为输出。
**注:**不像 _。pull()方法，此方法返回一个新数组。

**语法:**

```
_.without(array, [values])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要检查的数组。
*   **【值】:**此参数保存要排除的值。

**返回值:**这个方法返回新的过滤值数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var w = _.without([3.2, 5.2, 
       5.2, 1.2], 5.2, 3.2);    

// Use of _.without() method
let gfg = _.without(w);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 1.2 ]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var w = _.without([3, 5, 5, 1], 1, 3);    
var t = _.without([4, 7, 4, 8], 7, 4);

// Use of _.without() method
let gfg = _.without(w);
let gfg1 = _.without(t);

// Printing the output 
console.log(gfg);
console.log(gfg1);
```

**输出:**

```
[ 5, 5 ]
[ 8 ]

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var w = _.without(['a', 'b', 
        'c', 'b' ], 'a', 'b'); 
var x = _.without(['C++', 'Java', 
    'Python', '.Net' ], 'C++', 'Java');

// Use of _.without() method
let gfg = _.without(w);
let gfg2 = _.without(x);

// Printing the output 
console.log(gfg);
console.log(gfg2);
```

**输出:**

```
[ 'c' ]
[ 'Python', '.Net' ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。