# 洛达什 _。符合()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-conformsto-method/](https://www.geeksforgeeks.org/lodash-_-conformsto-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。conformsTo()** 方法通过调用源的谓词属性与对象的对应属性值，来检查给定对象是否符合给定的源。如果符合则返回真，否则返回假。

**语法:**

```
_.conformsTo( object, source )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存要检查的对象。
*   **来源:**此参数保存属性谓词要符合的对象。

**返回值:**如果对象符合，则该方法返回 true，否则返回 false。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Initializing a object
var object = { 'gfg': 5, 'GFG': 10 };

// Calling the _.conformsTo() functions
_.conformsTo(object, 
    { 'gfg': function(n)
        { return n > 1; } 
    }
);
```

**输出:**

```
true

```

**例 2:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Initializing a object
var object = { 'gfg': 5, 'GFG': 10 };

// Calling the _.conformsTo() functions
_.conformsTo(object, 
    { 'GFG': function(n) 
        { return n > 12; }
    }
);
```

**输出:**

```
false
```