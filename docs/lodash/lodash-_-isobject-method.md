# 洛达什 _。isObject()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isobject-method/](https://www.geeksforgeeks.org/lodash-_-isobject-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isObject()** 方法用于查找给定值是否为对象。如果给定值参数是一个对象，则返回布尔值“真”，否则返回“假”。

**语法:**

```
_.isObject(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

R **返回值:**如果值是一个对象，这个方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isObject()  
// method 

console.log(_.isObject('GeeksforGeeks')); 
console.log(_.isObject(1)); 
console.log(_.isObject([1, 2, 3]));
```

**输出:**

```
false
false
true
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isObject()  
// method 

console.log(_.isObject({})); 
console.log(_.isObject(null)); 
console.log(_.isObject(_.noop)); 
```

**输出:**

```
true
false
true
```