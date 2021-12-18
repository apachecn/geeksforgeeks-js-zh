# 洛达什 _。更新用()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-updatewith-method/](https://www.geeksforgeeks.org/lodash-_-updatewith-method/)

**_。updateWith()** **方法**接受一个定制函数，调用该函数来产生路径的对象。如果定制函数返回未定义的路径，则由方法来处理创建。它几乎和 _。update()函数。

**语法:**

```
_.updateWith(object, path, updater, [customizer])

```

**参数:**该方法接受上述四个参数，描述如下:

*   **Object:** This parameter stores the object to be modified.
*   **Path:** This parameter stores the path of the attribute to be set. It will be an array or a string.
*   **updater:** This is a function that generates an updated value.
*   **Customizer:** This parameter stores the function of custom assignment.

**返回值:**该方法返回对象。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = {};

// Use of _.updateWith() method 
let gfg = _.updateWith(obj, '[0][1]',
    _.constant('y'), Object);

// Returning the new object
console.log(gfg);
```

**输出:**

```
{ '0': { '1': 'y' } }

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 3 } }] };

// Use of _.updateWith() method 
_.updateWith(obj, 'cpp[0].java.python', 
    function(n) { return n * n; });

// Returning the updated object value
console.log(obj.cpp[0].java.python);
```

**输出:**

```
9
```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。