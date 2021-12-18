# 洛达什 _。调用()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-invoke-method/](https://www.geeksforgeeks.org/lodash-_-invoke-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。调用()方法**是调用对象路径上的方法。

**语法:**

```
_.invoke(object, path, args)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**保存要查询的对象。
*   **路径:**保存调用元素的方法的路径。
*   **参数:**调用方法的参数。

**返回值:**该方法返回被调用方法的结果。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = { 'p': [{ 'q': { 'r': [ 3, 5, 7, 9 ] } }] };

// Using the _.invoke() method
let invt_elem = _.invoke(object, 'p[0].q.r.slice', 3, 7);

// Printing the output 
console.log(invt_elem);
```

**输出:**

```
[ 9 ]

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = { 'p': [{ 'q': { 'r': { 's': [ 2, 4, 6, 8, 10 ] 

} } }] };

// Using the _.invoke() method
let invt_elem = _.invoke(object, 'p[0].q.r.s.slice', 2, 5);

// Printing the output 
console.log(invt_elem);
```

**输出:**

```
[ 6, 8, 10 ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。