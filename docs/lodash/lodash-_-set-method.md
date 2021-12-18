# 洛达什 _。设置()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-set-method/](https://www.geeksforgeeks.org/lodash-_-set-method/)

**_。set()** **方法**用于设置对象路径处的值，并返回一个新的 set 对象。

**语法:**

```
_.set(object, path, value)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**此参数保存要修改的对象。
*   **路径:**此参数保存要设置的属性的路径。它将是数组或字符串。
*   **值:**该参数保存要设置的值。

**返回值:**该方法返回新的集合对象。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 2012 } }] };

// set the value by _.set() method 
_.set(obj, 'cpp[0].java.python', 2020);

// return the new set object
console.log(obj.cpp[0].java.python);
```

**输出:**

```
2020

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 2012 } }] };

// set the value by _.set() method 
_.set(obj, ['html', '0', 'css', 'javascript'], 2024);

// return the new set object
console.log(obj.html[0].css.javascript);
```

**输出:**

```
2024

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#set