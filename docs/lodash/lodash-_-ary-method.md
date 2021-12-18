# 洛达什 _。ary()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ary-method/](https://www.geeksforgeeks.org/lodash-_-ary-method/)

**洛达什 _。ary()** 方法用于创建调用给定函数的函数，最多 n 个参数，忽略任何附加参数。

**语法:**

```
_.ary( func, n )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Function:** This parameter stores the function for which the upper limit of the parameter will be set.
*   **n:** This parameter stores the number n which element will be capped.

**返回值:**该方法返回新的封顶函数。

**注意:**如果你使用 0，它会覆盖每个元素。

下面的例子说明了 **Lodash _。ary()** 方法:

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");

// Applying _.ary() method
var gfg =_.map(['6', '8', '10'],
        _.ary(parseInt, 2));

console.log(gfg);
```

**输出:**

```
[ 6, NaN, 2 ]

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");

// Applying _.ary() method
var gfg =_.map(['6', '8', '10'], 
        _.ary(parseInt, 1));

console.log(gfg);
```

**输出:**

```
[ 6, 8, 10 ]
```

**参考:**T2】https://docs-lodash.com/v4/ary/