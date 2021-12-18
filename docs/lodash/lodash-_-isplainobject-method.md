# 洛达什 _。isPlainObject()方法

> 原文:[https://www . geesforgeks . org/lodash-_-isplayanobject-method/](https://www.geeksforgeeks.org/lodash-_-isplainobject-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。isPlainObject()方法**检查值是一个普通对象，这意味着一个由对象构造函数创建的对象还是一个[[原型]]为空的对象。

**语法:**

```
_.isPlainObject(value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**是用来校验值的函数。

**返回值:**如果值是普通对象，则该方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = _.isPlainObject(Object.create(null));

// Using the _.isPlainObject() method
let plain_data = ( object);

// Printing the output 
console.log(plain_data);
```

**输出:**

```
true

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = _.isPlainObject([1, 2, 3]);

// Using the _.isPlainObject() method
let plain_data = ( object);

// Printing the output 
console.log(plain_data);
```

**输出:**

```
false

```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = _.isPlainObject({ 'x': 0, 'y': 0 });

// Using the _.isPlainObject() method
let plain_data = ( object);

// Printing the output 
console.log(plain_data);
```

**输出:**

```
true

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。