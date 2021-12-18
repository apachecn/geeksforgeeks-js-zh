# Lodash _。sortedlastindexof()方法〔t1〕

> 哎哎哎:# t0]https://www . geeksforgeeks . org/LOD ash-_-sortedlastinindexof-method/

_。sortedLastIndexOf 方法用于返回数组中可以插入元素的最高索引，并保持其排序顺序。这个方法也像 _。lastIndexOf，除了它在排序的数组上执行二分搜索法。
**语法:**

```
_.sortedLastIndexOf(array, value)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要检查的数组。
*   **值:**此参数保存要搜索的值。

**返回值:**返回匹配值的索引，else -1。
**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array  
let y = [4, 5, 7, 7, 7]   

// Use of _.sortedLastIndexOf()  
// method  
let index = _.sortedLastIndexOf(y, 7); 

// Printing the output  
console.log(index);
```