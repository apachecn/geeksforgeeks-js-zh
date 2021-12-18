# 洛达什 _。逆变()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-invertby-method/](https://www.geeksforgeeks.org/lodash-_-invertby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。invertBy()方法**类似于 _。方法，除了反转的对象是通过迭代运行对象的每个元素的结果生成的。每个反转键对应的反转值也是一个负责生成反转值的键数组。

**语法:**

```
_.invertBy(object, iteratee)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**它持有对象反转每一个元素。
*   **迭代:**它保存方法每次迭代调用的函数。

**返回值:**该方法返回新的反转对象。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = { 'x': 3, 'y': 5, 'z': 3 };

// Using the _.invertBy() method
let invt_elem = _.invertBy(object);

// Printing the output 
console.log(invt_elem);
```

**输出:**

```
{ '3': ['x', 'z'], '5': ['y'] }

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = { 'x': 3, 'y': 5, 'z': 3 };

// Using the _.invertBy() method
let invt_elem = _.invertBy(object, function(value) {
  return 'group' + value;
});

// Printing the output 
console.log(invt_elem);
```

**输出:**

```
{ 'group3': ['x', 'z'], 'group5': ['y'] }

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。