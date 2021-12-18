# 洛达什 _。zipObjectDeep()方法

> 原文:[https://www . geeksforgeeks . org/lodash-_-zippobjectdeep-method/](https://www.geeksforgeeks.org/lodash-_-zipobjectdeep-method/)

_。zipObjectDeep()方法类似于 _。方法，除了它支持属性路径之外，它还接受两个数组，一个是属性标识符，一个是对应的值。

**语法:**

```
_.zipObjectDeep([props=[]], [values=[]])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **[prop = []] (array):** This parameter holds the attribute identifier.
*   **[value = []] (array):** This parameter holds the attribute value.

**返回值:**该方法返回新对象。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var obj1 = ['a.b[0].c', 'a.b[1].d'];

// Use of _.zipObjectDeep() method

let gfg = _.zipObjectDeep(obj1, [1, 2]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
{ a: { b: [ [ object ], [object] ] } }

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var obj1 = ([ 40, 30, 90 ]);

// Use of _.zipObjectDeep() method

let gfg = _.zipObjectDeep(obj1, [ 1, 2, 3 ]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
{ '30': 2, '40': 1, '90': 3 }

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var obj1 = (['a', 'g', 'h', 
    'b', 'c', 'd', 'e', 'f']);

// Use of _.zipObjectDeep() 
// method

let gfg = _.zipObjectDeep(obj1, 
        [1, 2, 3, 4, 5, 6, 7]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
{ a: 1, g: 2, h: 3, b: 4, c: 5, d: 6, e: 7, f: undefined }

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。