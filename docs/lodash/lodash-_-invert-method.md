# 洛达什 _。反转()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-invert-method/](https://www.geeksforgeeks.org/lodash-_-invert-method/)

**_。invent()****方法**用于返回对象的副本，其中对象键转换为值，对象值转换为键。如果对象包含重复值，后续值将覆盖属性分配。

**语法:**

```
_.invert(object)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **对象:**此参数保存要反转的对象。

**返回值:**该方法返回新的反转对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj =  { 'a': 1, 'b': 2, 'c': 3 };

// Use of _.invert method 
console.log(_.invert(obj)); 
```

**输出:**

```
{ '1': 'a', '2': 'b', '3': 'c'}

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj =  { 'a': 1, 'b': 2, 'c': 2 };

// Use of _.invert method 
console.log(_.invert(obj)); 
```

**输出:**

```
{ '1': 'a', '2': 'c' }

```

**例 3:**

## java 描述语言

```
/// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj = { 
            Name: "GeeksforGeeks", 
            password: "gfg@1234", 
            username: "your_geeks"
        } 

// Use of _.invert method 
console.log(_.invert(obj));
```

**输出:**

```
{GeeksforGeeks: "Name", 
gfg@1234: "password",
your_geeks: "username"}

```