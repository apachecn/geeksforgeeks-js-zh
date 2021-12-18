# 洛达什 _。uniqBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-uniqby-method/](https://www.geeksforgeeks.org/lodash-_-uniqby-method/)

_。uniqBy 方法类似于 _。uniq 的不同之处在于，它接受为数组中的每个元素调用的迭代，以生成计算唯一性的标准。结果值的顺序由它们在数组中出现的顺序决定。
**语法:**

```
_.uniqBy([array], [iteratee=_.identity])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **【数组】:**此参数保存要检查的数组。
*   **【迭代=_。identity](函数):**此参数保存每个元素调用的迭代。

**返回值:**此方法用于返回新的无重复数组。
**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let y = ([2.4, 1.6, 2.2, 1.3]);    

// Use of _.uniqBy() 
// method

let gfg = _.uniqBy(y, Math.floor);

// Printing the output 
console.log(gfg);
```