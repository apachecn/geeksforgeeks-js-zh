# 洛达什 _。hasIn()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-hasin-method/](https://www.geeksforgeeks.org/lodash-_-hasin-method/)

**_。hasIn()** **方法**用于检查路径是否是对象的直接或继承属性。如果路径存在，则返回真，否则返回假。

**语法:**

```
_.hasIn(object, path)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存要查询的对象。
*   **路径:**此参数保存要检查的路径。路径将是数组或字符串。

**返回值:**如果路径存在，该方法返回真，否则返回假

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var object =  _.create({ 'a': _.create({ 'b': 2 }) });

// Use of _.hasIn method 
console.log(_.hasIn(object, 'a')); 
console.log(_.hasIn(object, ['a'])); 
console.log(_.hasIn(object, ['b'])); 
```

**输出:**

```
true
true
false

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var object =  _.create({ 'a': _.create({ 'b': 2 }) });

// Use of _.hasIn method 
console.log(_.hasIn(object, 'a.b')); 
console.log(_.hasIn(object, ['a','b'])); 
console.log(_.hasIn(object, ['a','b','c'])); 
```

**输出:**

```
true
true
false

```