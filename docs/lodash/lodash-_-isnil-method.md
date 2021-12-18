# 洛达什 _。isNil()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnil-method/](https://www.geeksforgeeks.org/lodash-_-isnil-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

_ **。isNil()** 方法用于检查值是否为 null 或未定义。如果该值为 nullish，则返回 true，否则返回 false。

**语法:**

```
_.isNil(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值**:该参数保存要检查的值。

**返回值:**如果值为 nullish，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNil()  
// method 
let gfg = _.isNil(null);

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

// Use of _.isNil()  
// method 
let gfg = _.isNil(void 0);

// Printing the output  
console.log(gfg);
```

**输出:**

```
true
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNil()  
// method 
let gfg = _.isNil(NaN);

// Printing the output  
console.log(gfg);
```

**输出:**

```
false
```