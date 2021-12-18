# 洛达什 _。天花板()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ceil-method/](https://www.geeksforgeeks.org/lodash-_-ceil-method/)

**_。ceil()** 方法用于计算向上舍入到精确的数字。

**语法:**

```
_.ceil(number, [precision =  0])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数字:**此参数保存要向上舍入的数字。
*   **【精度= 0】:**此参数保存要向上舍入的精度。

**返回值:**此方法返回向上舍入的数字。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.ceil() method 
let gfg = _.ceil(2.4);

// Printing the output  
console.log(gfg)
```

**输出:**

```
3
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.ceil() method 
let gfg = _.ceil(3.005, 2);

// Printing the output  
console.log(gfg)
```

**输出:**

```
3.01
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.ceil() method 
let gfg = _.ceil(1680, -2);

// Printing the output  
console.log(gfg)
```

**输出:**

```
1700
```