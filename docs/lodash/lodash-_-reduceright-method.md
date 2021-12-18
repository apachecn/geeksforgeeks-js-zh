# 洛达什 _。reduceRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-reduceright-method/](https://www.geeksforgeeks.org/lodash-_-reduceright-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。reduceRight()方法类似于 _。reduce()方法，只是它从右向左迭代集合的元素。

**语法:**

```
_.reduceRight(collection, iteratee, accumulator)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**此参数保存每次迭代调用的函数。
*   **累加器:**此参数保存初始值。

**返回值:**此方法返回累计值。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = [[10, 11], [12, 13], [14, 15]];

// Use of _.reduceRight() method

let gfg = _.reduceRight(array, 
    function(flattened, other) {
  return flattened.concat(other);
}, []);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 14, 15, 12, 13, 10, 11 ]

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = [['C++', 'C#'], 
    ['DAA', 'Java'], ['Lodash', 'Python']];

// Use of _.reduceRight() method

let gfg = _.reduceRight(array, 
    function(flattened, other) {
  return flattened.concat(other);
}, []);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 'Lodash', 'Python', 'DAA', 'Java', 'C++', 'C#' ]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。