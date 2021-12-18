# 洛达什 _。isSymbol()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-issymbol-method/](https://www.geeksforgeeks.org/lodash-_-issymbol-method/)

**_。isSymbol()** 方法用于查找给定值是否为符号对象。如果给定值是符号对象，则返回真。否则，它返回 false。

**语法:**

```
_.isSymbol(value)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值是符号，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isSymbol() method 
console.log(_.isSymbol('geeksforgeeks')); 
```

**输出:**

```
false

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isSymbol() method 
console.log(_.isSymbol(Symbol())); 
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

// Use of _.isSymbol() method 
console.log(_.isSymbol(Symbol.iterator)); 
```

**输出:**

```
true

```