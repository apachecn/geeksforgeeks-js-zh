# 洛达什 _。时代()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-times-method/](https://www.geeksforgeeks.org/lodash-_-times-method/)

洛达什 **_。times()方法**调用迭代 n 次，返回每次调用结果的数组。使用一个参数调用迭代。

**语法:**

```
_.times( n, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **n:** The number of times the iterative function is called.
*   **Iteration:** The function called in each iteration.

**返回值:**返回结果数组。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.times() method 
// by taking n=5 and string
let gfg = _.times(5,String); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
["0", "1", "2", "3", "4"]

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.times() method 
// by taking n=3 and constant method
let gfg = _.times(3,_.constant(5)); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
[5, 5, 5]

```