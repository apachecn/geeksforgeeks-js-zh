# 洛达什 _。get()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-get-method/](https://www.geeksforgeeks.org/lodash-_-get-method/)

**_。get()** **方法**用于获取对象路径上的值。如果解析的值未定义，将返回默认值。

**语法:**

```
_.get(object, path, [defaultValue])

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**此参数保存要查询的对象。
*   **路径:**此参数保存要获取的属性的路径。路径将是数组或字符串。
*   **默认值:**此参数保存未定义的解析值的返回值。

**返回值:**该方法返回解析值。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var object = { 'c': [{ 'python': { 'java': 3 } }] };

// Use of _.get method 
console.log(_.get(object, 'c[0].python.java')); 
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

// Given object
var object = { 'c': [{ 'python': { 'java': 3 } }] };

// Use of _.get method 
console.log(_.get(object, ['c', '0', 'python', 'java'])); 
```

**输出:**

```
3

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var object = { 'c': [{ 'python': { 'java': 3 } }] };

// Use of _.get method 
console.log(_.get(object, 'c.python.java', 'default')); 
```

**输出:**

```
'default'

```