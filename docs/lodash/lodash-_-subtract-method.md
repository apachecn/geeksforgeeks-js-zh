# 洛达什 _。减法()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-subtract-method/](https://www.geeksforgeeks.org/lodash-_-subtract-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

_ **。减法()**方法用于减去两个数字。

**语法:**

```
_.subtract(minuend, subtrahend)
```

**参数**:该方法接受两个参数，如上所述，如下所述:

*   **被减数:**此参数保存减法中的第一个数字。
*   **减数:**此参数保存减法中的第二个数。

**返回值:**这个方法返回两个数的差。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.subtract() method 
let gfg = _.subtract(50, 18); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
32
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.subtract() method 
let gfg = _.subtract(87, -98); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
185
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.subtract() method 
let gfg = _.subtract(-126, -53); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
-73
```