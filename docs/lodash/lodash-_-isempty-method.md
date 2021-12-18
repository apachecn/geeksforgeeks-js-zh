# 洛达什 _。isEmpty()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isempty-method/](https://www.geeksforgeeks.org/lodash-_-isempty-method/)

洛达什 **_。isEmpty()方法** 检查值是否为空对象、集合、地图或集合。 对象如果没有自己的可枚举字符串键控属性，则被认为是空的。如果集合的长度为 0，则它们被认为是空的。同样，如果地图和集合的大小为 0，则它们被认为是空的。

**语法:**

```
_.isEmpty( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter stores the value that needs to be checked as null.

**返回值:**该方法返回一个**布尔值**(如果给定值为空，则返回真，否则返回假)。

**例 1:** 当值为空时，该方法返回 **真** 。

```
// Defining Lodash variable
const _ = require('lodash'); 

// Checking for Empty Value
console.log("The Value is Empty : "
        +_.isEmpty(null));
```

**输出:**

```
The Value is Empty : true
```

**例 2:** 当数组为空时，此方法返回 **真** 。

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = []

// Checking for Empty Value
console.log("The Value is Empty : "
        +_.isEmpty(val));
```

**输出:**

```
The Value is Empty : true
```

**例 3:** 该方法返回 **真**为布尔值。

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = false;

// Checking for Empty Value
console.log("The Value is Empty : " 
        +_.isEmpty(val));
```

**输出:**

```
The Value is Empty : true
```

**例 4:** 在 t 他的例中，该方法将返回**假** 。

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = { "a": 1 };

// Checking for Empty Value
console.log("The Value is Empty : " 
        +_.isEmpty(val)); 
```

**输出:**

```
The Value is Empty : false
```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。

可以使用`npm install lodash.` 安装洛达斯库