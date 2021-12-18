# 洛达什 _。isFunction()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isfunction-method/](https://www.geeksforgeeks.org/lodash-_-isfunction-method/)

洛达什 **_。isFunction()方法**检查给定值是否为函数对象，并返回相应的布尔值。

**语法:**

```
_.isFunction( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**该参数保存要检查的函数对象的值。

**返回值:**该方法返回一个**布尔值**(如果给定值是函数对象号，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

function Geeks(){
    var a="gfg";
}
// Checking for Function
console.log("The Value is Function : "
        + _.isFunction(Geeks));
```

**输出:**

```
The Value is Function : true

```

**例 2:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Function
console.log("The Value is Function : "
        + _.isFunction("Function"));
```

**输出:**

```
The Value is Function : false

```

**例 3:** 对于 _ object，返回 true。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Function
console.log("The Value is Function : "
        + _.isFunction(_));
```

**输出:**

```
The Value is Function : true

```