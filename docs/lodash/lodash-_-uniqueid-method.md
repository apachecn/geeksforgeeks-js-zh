# 洛达什 _。uniqueId()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-uniqueid-method/](https://www.geeksforgeeks.org/lodash-_-uniqueid-method/)

洛达什 **_。uniqueId()方法**用于每次为某个元素创建一个唯一的 Id。这种方法适用于为大多数用例分配唯一的 id，但不适用于复杂的项目，即使项目重新启动，这些项目也总是需要唯一的 id。

**语法:**

```
_.uniqueId(prefix)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **Prefix:** The value as the identification prefix.

**返回值:**该方法返回字符串唯一标识。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.uniqueId()  
// Method without the prefix
let gfg = _.uniqueId(); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
1

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.uniqueId()  
// Method with prefix
let ans = _.uniqueId("gfg_"); 

// Printing the output  
console.log(ans); 

let ans1 = _.uniqueId("gfg_"); 

// Printing the output  
console.log(ans1);
```

**输出:**

```
gfg_1
gfg_2

```