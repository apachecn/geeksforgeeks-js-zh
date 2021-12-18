# 洛达什 _。unionBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unionby-method/](https://www.geeksforgeeks.org/lodash-_-unionby-method/)

**_。unionBy()** 方法接受为每个数组的每个元素调用的迭代，以生成计算唯一性的标准。结果值的顺序由值出现的第一个数组决定。

**语法:**

```
_.unionBy(array, [iteratee = _.identity])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要检查的数组。
*   **【迭代= _。identity]:** 此参数保存每个元素调用的迭代。

**返回值:**此方法用于返回新的组合值数组。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.unionBy() method 
let gfg = _.unionBy([{ 'y': 1 }], 
                    [{ 'y': 2 }, { 'y': 1 }], 
                    [{ 'y': 3 }], 'y'); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[ { 'y': 1 }, { 'y': 2 }, {'y': 3} ]
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.unionBy() method 
let gfg = _.unionBy([1.5], 
                    [2.6, 2.7],
                    [2.3, 3.8], Math.floor); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[1.5, 2.6, 3.8]
```