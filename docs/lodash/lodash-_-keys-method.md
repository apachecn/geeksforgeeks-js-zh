# 洛达什 _。按键()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-keys-method/](https://www.geeksforgeeks.org/lodash-_-keys-method/)

**_。keys()** **方法**用于返回给定对象的所有键的列表。

**语法:**

```
_.keys(object)

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Object:** This parameter stores object elements.

**返回值:**这个方法返回给定对象的所有键的数组。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj =  { 'a': 1, 'b': 2, 'c': 2 };

// Use of _.keys method 
console.log(_.keys(obj));
```

**输出:**

```
['a', 'b', 'c']

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj = { 
            Name: "GeeksforGeeks", 
            password: "gfg@1234", 
            username: "your_geeks"
        } 

// Use of _.keys method 
console.log(_.keys(obj));
```

**输出:**

```
["Name", "password", "username"]

```