# 洛达什 _。isString()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isstring-method/](https://www.geeksforgeeks.org/lodash-_-isstring-method/)

**_。isString()** 方法用于查找给定值是否为字符串对象。如果给定值是字符串，则返回真。否则，它返回 false。

**语法:**

```
_.isString(value)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值是字符串，这个方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isString() method 
console.log(_.isString('GeeksforGeeks')); 
console.log(_.isString(true)); 
```

**输出:**

```
true
false

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isString() method 
console.log(_.isString('123')); 
console.log(_.isString(123)); 
console.log(_.isString("0.123")); 
```

**输出:**

```
true
false
true

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。