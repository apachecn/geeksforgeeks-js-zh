# 洛达什 _。toPath()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-topath-method/](https://www.geeksforgeeks.org/lodash-_-topath-method/)

洛达什 **_。toPath()方法**用于将给定值转换为属性路径数组。

**语法:**

```
_.toPath(value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** The value to be converted into a path array.

**返回值:**新属性路径数组。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.toPath() method 
let gfg = _.toPath('geeks.for.geeks'); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
["geeks", "for", "geeks"]
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.toPath() method 
let gfg = _.toPath('geeks[0].for[1].geeks[2]'); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
["geeks", "0", "for", "1", "geeks", "2"]

```