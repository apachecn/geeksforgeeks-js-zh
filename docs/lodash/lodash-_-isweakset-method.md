# 洛达什 _。isWeakSet()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isweakset-method/](https://www.geeksforgeeks.org/lodash-_-isweakset-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。iswakeset()**方法用于查找给定值是否为 WeakSet 对象。如果给定值是 weakset 对象，则返回 true。否则，它返回 false。

**语法:**

```
_.isWeakSet( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值为弱集，则该方法返回 true，否则返回 false。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isWeakSet() method 
console.log(_.isWeakSet(new Set));
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

// Use of _.isWeakSet() method 
console.log(_.isWeakSet(new WeakSet));
```

**输出:**

```
true

```