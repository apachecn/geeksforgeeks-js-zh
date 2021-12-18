# 洛达什 _。更新()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-update-method/](https://www.geeksforgeeks.org/lodash-_-update-method/)

**_。更新()** **方法**接受更新器产生的值进行设置。这个方法使用 _。函数来自定义路径创建。几乎和 _。set()函数。

**语法:**

```
_.update(object, path, updater)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**此参数保存要修改的对象。
*   **路径:**此参数保存要设置的属性的路径。它将是数组或字符串。
*   **更新器:**这是产生更新值的函数。

**返回值:**该方法返回新对象。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 3 } }] };

// Use of _.update() method 
_.update(obj, 'cpp[0].java.python', 
    function(n) { return n * n; });

// return the new object
console.log(obj.cpp[0].java.python);
```

**输出:**

```
9

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object 
var obj = { 'cpp': [{ 'java': { 'python': 3 } }] };

// Use of _.update() method 
_.update(obj, 'html[0].css.javascript', 
    function(n) { return n ? n + 1 : 0; });

// return the new object
console.log(obj.html[0].css.javascript);
```

**输出:**

```
0

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#update