# 洛达什 _。lte()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-lte-method/](https://www.geeksforgeeks.org/lodash-_-lte-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。lte()方法**检查值是否小于或等于其他值。

**语法:**

```
_.lte(value, other)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**该参数保存用于比较的第一个值。
*   **其他:**此参数保存与其他值比较的其他值。

**返回值:**如果值小于或等于其他值，则该方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var num = _.lte(16, 16);

// Using the _.lte() method
let less_eq_elem = ( num );

// Printing the output 
console.log(less_eq_elem);
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
var num = _.lte(34, 76);

// Using the _.lte() method
let less_eq_elem = ( num );

// Printing the output 
console.log(less_eq_elem);
```

**输出:**

```
true

```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var num = _.lte(81, 46);

// Using the _.lte() method
let less_eq_elem = ( num );

// Printing the output 
console.log(less_eq_elem);
```

**输出:**

```
false

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。