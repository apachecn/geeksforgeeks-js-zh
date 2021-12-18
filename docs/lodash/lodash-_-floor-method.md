# 洛达什 _。地板()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-floor-method/](https://www.geeksforgeeks.org/lodash-_-floor-method/)

**_。floor()** 方法用于计算向下舍入到精确值的数字意味着它向下舍入到 floor 值。

**语法:**

```
_.floor(number, [precision = 0])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数字:**此参数保存要向下舍入的数字。
*   **【精度= 0】:**此参数保存要向下舍入到的精度。

**返回值:**此方法返回向下舍入的数字。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.floor() method 
let gfg = _.floor(2.4);

// Printing the output  
console.log(gfg)
```

**输出:**

```
2
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.floor() method 
let gfg = _.floor(0.525, 2);

// Printing the output  
console.log(gfg)
```

**输出:**

```
0.52
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.floor() method 
let gfg = _.floor(1680, -2);

// Printing the output  
console.log(gfg)
```

**输出:**

```
1600
```