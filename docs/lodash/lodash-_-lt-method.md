# 洛达什 _。lt()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-lt-method/](https://www.geeksforgeeks.org/lodash-_-lt-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。lt()方法**检查值是否小于另一个值。

**语法:**

```
_.lt(value, other)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**该参数保存第一个需要比较的值。
*   **其他:**此参数保存与之比较的其他值。

**返回值:**如果值小于其他值，该方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var num = _.lt(34, 67);

// Using the _.lt() method
let less_elem = ( num );

// Printing the output 
console.log(less_elem);
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
var num = _.lt(77, 77);

// Using the _.lt() method
let less_elem = ( num );

// Printing the output 
console.log(less_elem);
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
var num = _.lt(56, 36);

// Using the _.lt() method
let less_elem = ( num );

// Printing the output 
console.log(less_elem);
```

**输出:**

```
false

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。