# 洛达什 _。变换()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-transform-method/](https://www.geeksforgeeks.org/lodash-_-transform-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。
**_。变换()方法**是 _。reduce()方法将对象转换为一个新的累加器对象，这是通过迭代运行它自己的每个可枚举字符串键控属性的结果，每次调用都可能使累加器对象发生变化。如果不提供累加器，将使用具有相同原型的新对象。
**语法:**

```
_.transform(object, iteratee, accumulator)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**它保存要迭代的对象。
*   **迭代:**是方法每次迭代为每个元素调用的函数。
*   **累加器:**保存自定义累加器值。

**返回值:**此方法返回累计值。
**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library
const _ = require("lodash");

// Original array
var object = [12, 13, 14];    

// Using the _.transform() method
let st_elem = _.transform(object,
            function(result, n) {
  result.push(n *= n);
  return n % 2 == 0;
}, []);

// Printing the output
console.log(st_elem);
```