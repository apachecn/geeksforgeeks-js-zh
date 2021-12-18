# 洛达什 _。isUndefined()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isundefined-method/](https://www.geeksforgeeks.org/lodash-_-isundefined-method/)

**_。isUndefined()** 方法用于查找给定值是否未定义。如果给定值未定义，则返回**真**。否则，返回**假**。

**语法:**

```
_.isUndefined(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述。

*   **值:**该参数保存要检查的值。

**返回值:**此方法返回 **true** 如果值未定义，否则 **false** 。

**示例 1:** 在以下示例中，*const _ = require(“lodash”)*用于将 **lodash** 库导入到文件中。

## java 描述语言

```
// The lodash library is included 
const _ = require("lodash");  

// Use of _.isUndefined() method 
console.log(_.isUndefined(null)); 
console.log(_.isUndefined(void 0)); 
console.log(_.isUndefined('gfg')); 
```

**输出:**

```
false
true
false

```

**例 2:**

## java 描述语言

```
// The lodash library is included
const _ = require("lodash");  

// Use of _.isUndefined() method 
console.log(_.isUndefined(window.missingVariable)); 
console.log(_.isUndefined(10)); 
console.log(_.isUndefined(undefined)); 
```

**输出:**

```
true
false
true

```