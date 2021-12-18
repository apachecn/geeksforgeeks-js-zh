# 洛达什 _。sortedIndexOf()方法

> 原文:[https://www . geeksforgeeks . org/lodash-_-sorted indexof-method/](https://www.geeksforgeeks.org/lodash-_-sortedindexof-method/)

**_。sortedIndexOf()方法**用于获取排序数组中特定元素第一次出现的索引。它使用二分搜索法对数组进行排序。

**语法:**

```
_.sortedIndexOf(array, value)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the sorted array.
*   **Value:** This parameter stores the value to be evaluated.

**返回值:**该方法返回该值应该插入数组的索引，其他返回-1。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let x = [1, 2, 3, 4, 4, 4, 5, 6, 6]  

// Use of _.sortedIndexOf() 
// method 
let index = _.sortedIndexOf(x, 4);

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

// Use of _.sortedIndexOf() 
// method 
let index = _.sortedIndexOf(x, 'e');

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

// Use of _.sortedIndexOf() 
// method 
let index = _.sortedIndexOf(x, 'luby');

// Printing the output 
console.log(index);
```

**输出:**

```
-1

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。