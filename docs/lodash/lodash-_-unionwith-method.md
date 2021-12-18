# 洛达什 _。unionWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unionwith-method/](https://www.geeksforgeeks.org/lodash-_-unionwith-method/)

**_。unionWith()** 方法接受比较器，调用该比较器来比较数组的元素。结果值的顺序由值出现的第一个数组决定。使用两个参数调用比较器:(arrVal、othVal)。

**语法:**

```
_.unionWith(array, [comparator])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要检查的数组。
*   **【比较器】:**该参数保存每个元素调用的比较器。

**返回值:**此方法用于返回新的组合值数组。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array
var objects = [{ 'a': 1, 'b': 2 }];
var others = [{ 'b': 2 }];

// Use of _.unionWith() method 
let gfg = _.unionWith(objects, others, _.isMatch); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[{'a': 1, 'b': 2 }, { 'b': 2}]
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }];
var others = [{ 'x': 1, 'y': 1 }, { 'x': 1, 'y': 2 }];

// Use of _.unionWith() method 
let gfg = _.unionWith(objects, others, _.isEqual); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }, { 'x': 1, 'y': 1 }]
```