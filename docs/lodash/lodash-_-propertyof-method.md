# 洛达什 _。()方法属性

> 原文:[https://www.geeksforgeeks.org/lodash-_-propertyof-method/](https://www.geeksforgeeks.org/lodash-_-propertyof-method/)

洛达什 **_。** **法**是 _ 的逆。property()函数。此函数将对象作为参数，并返回一个函数，该函数将返回所提供属性的值。

**语法:**

```
_.property( object )
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **对象:**该参数保存该方法需要返回的对象的值。

**返回值:**这个方法返回一个新的访问器函数。

**例 1 :**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

var info = { 
            Company: 'GeeksforGeeks', 
            Address: 'Noida'
        }; 

// Use of _.propertyOf() method         
let gfg = _.propertyOf(info)('Company')

// Printing the output  
console.log(gfg);
```

**输出:**

```
GeeksforGeeks

```

**例 2 :**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

var array = [0, 2],
    object = { 'a': array, 'b': array };

// Use of _.propertyOf() method         
let gfg = _.map(['a[0]', 'b[1]'], _.propertyOf(object)); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
[0, 2]

```