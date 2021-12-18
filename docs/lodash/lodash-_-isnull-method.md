# 洛达什 _。isNull()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnull-method/](https://www.geeksforgeeks.org/lodash-_-isnull-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isNull()** 方法用于查找对象的值是否为 Null。如果该值为 null，则返回 true，否则返回 false。

**语法:**

```
_.isNull(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值为空，则该方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNull()  
// method 
let gfg = _.isNull(null);

// Printing the output  
console.log(gfg);
```

**输出:**

```
true
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNull()  
// method 
let gfg = _.isNull(void 0);

// Printing the output  
console.log(gfg);
```

**输出:**

```
false
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNull()  
// method 
let gfg = _.isNull(NaN);

// Printing the output  
console.log(gfg);
```

**输出:**

```
false
```