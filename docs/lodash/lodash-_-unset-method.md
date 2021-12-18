# 洛达什 _。取消设置()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-unset-method/](https://www.geeksforgeeks.org/lodash-_-unset-method/)

洛达什 **_。unset()** **方法**用于移除对象路径处的属性。如果属性被移除，则返回真值，否则返回假值。

**语法:**

```
_.unset(object, path)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Object:** This parameter stores the object to be modified.
*   **Path:** This parameter stores the path of the attribute to be unset. It can be an array or a string.

**返回值:**此方法返回 **true** 如果属性被删除，否则 **false** 。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 3 } }] };

// Use of _.unset() method
console.log(_.unset(obj, 'cpp[0].java.python'));

// Object is modified
console.log(obj);
```

**输出:**

```
true
{ cpp: [ { java: {} } ] }

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 3 } }] };

// Use of _.unset() method
console.log(_.unset(obj, ['html', 'css', 'javascript']));

// Object
console.log(obj);
```

**输出:**

```
true
{ cpp: [ { java: [Object] } ] }

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash并且可以使用 npm 安装 lodash 来安装。。