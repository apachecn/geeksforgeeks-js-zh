# 洛达什 _。sortedIndex()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sortedindex-method/](https://www.geeksforgeeks.org/lodash-_-sortedindex-method/)

**_。sortedIndex()方法**用于返回数组中可以插入元素的最低索引，并保持其排序顺序。它使用二分搜索法。

**语法:**

```
_.sortedIndex(array, value)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the sorted array.
*   **Value:** This parameter stores the value to be evaluated.

**返回值:**该方法返回值应该插入数组的索引。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let x = [1, 2, 3, 4, 4, 4, 5, 6, 6]  

// Use of _.sortedIndex() 
// method 
let index = _.sortedIndex(x, 4);

// Printing the output 
console.log(index);
```

**输出:**

```
3

```

**例二:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let x = ['a', 'b', 'c', 'd', 'e', 'e', 'e', 'f']  

// Use of _.sortedIndex() 
// method 
let index = _.sortedIndex(x, 'e');

// Printing the output 
console.log(index);
```

**输出:**

```
4

```

**例三:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let x = ['ajax', 'django', 'mongoDb',  
       'react', 'reactnative', 'yarn']  

// Use of _.sortedIndex() 
// method 
let index = _.sortedIndex(x, 'ruby');

// Printing the output 
console.log(index);
```

**输出:**

```
5

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。