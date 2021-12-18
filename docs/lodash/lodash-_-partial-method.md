# 洛达什 _。部分()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-partial-method/](https://www.geeksforgeeks.org/lodash-_-partial-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。partial()** **方法**用于创建一个函数，该函数调用给定的*函数*函数，并在其接收的参数前添加*partial*。

**语法:**

```
_.partial( func, partials )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **函数:**此参数保存部分应用参数的函数。
*   **分音:**此参数保存要应用的参数。这是一个可选参数。

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

// Using the _.partial() method  
var call_gfg =
  _.partial(info, 'GeeksforGeeks');
call_gfg('is a computer science portal for geeks');
```

**输出:**

```
'GeeksforGeeks is a computer science portal for geeks'
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

// Using the _.partial() method  
var say_gfg = _.partial(info, _, 'geeks');
say_gfg('Hello');
```

**输出:**

```
'Hello geeks'
```