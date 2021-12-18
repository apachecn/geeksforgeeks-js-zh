# 洛达什 _。partialRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-partialright-method/](https://www.geeksforgeeks.org/lodash-_-partialright-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。partially()****方法**用于创建一个函数，该函数调用给定的*函数*函数，并将*partially*附加到它接收的参数上。几乎和 _。partial()函数。

**语法:**

```
_.partialRight( func, partials )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **函数:**此参数保存要部分应用参数的函数。
*   **部分:**此参数保存要部分应用的参数。这是一个可选参数。

**返回值:**该方法返回新的部分应用函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given Function
function info(information, name) {
  console.log(information + ' ' + name);
}

// Using the _.partialRight() method  
var call_gfg =
  _.partialRight(info,
    'is a computer science portal');
call_gfg('GeeksforGeeks');
```

**输出:**

```
'GeeksforGeeks is a computer science portal'
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given Function
function info(information, name) {
  console.log(information + ' ' + name);
}

// Using the _.partialRight() method
// with placeholders
var say_gfg = 
  _.partialRight(info, 'Hello',  _);
say_gfg('geeks');
```

**输出:**

```
'Hello geeks'
```