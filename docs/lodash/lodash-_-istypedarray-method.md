# 洛达什 _。isTypedArray()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-istypedarray-method/](https://www.geeksforgeeks.org/lodash-_-istypedarray-method/)

**_。isTypedArray()** **方法**用于查找给定值是否为类型化数组。如果给定值是类型化数组，则返回真。否则，它返回 false。

**语法:**

```
_.isTypedArray(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值是类型化数组，该方法返回 true，否则返回 false。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isTypedArray() method  

// Passing a array as an argument
console.log(_.isTypedArray([])); 

// Passing an array with value as an argument
console.log(_.isTypedArray([1, 2, 3, 4]));
```

**输出:**

```
false
false

```

**例 2:**

```
// Requiring the lodash library  
const _ = require("lodash");      

// Use of _.isTypedArray() method 

// Passing a typedArray objects Int8Array
console.log(_.isTypedArray(new Int8Array(8)));

// Passing a typedArray objects Float64Array
console.log(_.isTypedArray(new Float64Array()));
```

**输出:**

```
true
true

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考资料:**[https://lodash . com/docs/4 . 17 . 15 # istypdarray](https://lodash.com/docs/4.17.15#isTypedArray)