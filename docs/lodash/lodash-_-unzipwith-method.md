# 洛达什 _。解压()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unzipwith-method/](https://www.geeksforgeeks.org/lodash-_-unzipwith-method/)

**_。unzipcwith()**方法接受迭代来指定应该如何组合重新分组的值。迭代是用每个组的元素调用的。

**语法:**

```
_.unzipWith(array, [iteratee = _.identity])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array of grouping elements to be processed.
*   **[iteration = _]. ID]:** This parameter holds the function of combining reorganization values.

**返回值:**这个方法返回重组元素的新数组。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Original array
var zipped_arr = _.zip([15, 7], [185, 20], [478, 123]);

// Use of _.unzipWith() method 
let gfg = _.unzipWith(zipped_arr, _.subtract);

// Printing the output  
console.log(gfg)
```

**输出:**

```
[8, 165, 355]
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Original array
var zipped_arr = _.zip([4, 9], [185, 20], [478, 123]);

// Use of _.unzipWith() method 
let gfg = _.unzipWith(zipped_arr, _.add);

// Printing the output  
console.log(gfg)
```

**输出:**

```
[13, 205, 601]
```