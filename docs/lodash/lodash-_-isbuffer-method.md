# 洛达什 _。isBuffer()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isbuffer-method/](https://www.geeksforgeeks.org/lodash-_-isbuffer-method/)

洛达什 **_。方法** 检查给定值是否为缓冲区。

**语法:**

```
_.isBuffer( value )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter stores the value of the buffer to be checked.

**返回值:**该方法返回一个**布尔值**(如果给定值是一个缓冲区，则返回真，否则返回假)。

**示例 1:** 当值为 Buffer 时，此方法返回 **true** 。

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = new Buffer(2);

// Checking for Buffer
console.log("The Value is Buffer : " 
        +_.isBuffer(val));
```

**输出:**

```
The Value is Buffer : true

```

**例 2:**

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = new Uint8Array(2);

// Checking for Buffer
console.log("The Value is Buffer : " 
        +_.isBuffer(val));
```

**输出:**

```
The Value is Buffer : false

```