# 洛达什 _。has()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-has-method/](https://www.geeksforgeeks.org/lodash-_-has-method/)

**_。has()** **方法**用于检查路径是否是对象的直接属性。如果路径存在，则返回真，否则返回假。

**语法:**

```
_.has(object, path)

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
var object = { 'a': { 'b': 2 } };

// Use of _.has method 
console.log(_.has(object, 'a')); 
console.log(_.has(object, ['a'])); 
console.log(_.has(object, ['b'])); 
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
var object = { 'a': { 'b': 2 } };

// Use of _.has method 
console.log(_.has(object, 'a.b')); 
console.log(_.has(object, ['a','b'])); 
console.log(_.has(object, ['a','b','c'])); 
```

**输出:**

```
true
true
false

```