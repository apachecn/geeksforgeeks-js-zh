# 洛达什 _。toArray()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-toarray-method/](https://www.geeksforgeeks.org/lodash-_-toarray-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。toArray()** 方法用于将给定值转换为数组。

**语法:**

```
_.toArray( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**这个方法返回转换后的数组。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toArray() method 
console.log(_.toArray(null)); 
console.log(_.toArray('gfg'));
```

**输出:**

```
[]
['g', 'f', 'g']

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toArray() method 
console.log(_.toArray(10)); 
console.log(_.toArray({ 'html': 1, 
    'css': 2, 'javascript': 3 }));
```

**输出:**

```
[]
[1, 2, 3]

```