# 洛达什 _。zip()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-zip-method/](https://www.geeksforgeeks.org/lodash-_-zip-method/)

**_。zip()** 方法用于创建分组元素的数组，第一个包含给定数组的第一个元素，第二个包含给定数组的第二个元素，以此类推。

**语法:**

```
_.zip([arrays])
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **【数组】:**此参数保存要处理的数组。

**返回值:**这个方法返回重组元素的新数组。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.zip() method 
let gfg = _.zip(['a', 'b', 'c'], 
                [1, 2, 3], 
                [true, false, true]);

// Printing the output  
console.log(gfg)
```

**输出:**

```
a,1,true,b,2,false,c,3,true
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.zip()  
// method 
let gfg = _.zip(['Amit', 'Akash', 'Avijit'], 
                [1, 2, 3], 
                ['pass', 'pass', 'fail']);

// Printing the output  
console.log(gfg)
```

**输出:**

```
Amit,1,pass,Akash,2,pass,Avijit,3,fail
```