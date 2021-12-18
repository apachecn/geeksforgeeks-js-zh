# 洛达什 _。isSet()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isset-method/](https://www.geeksforgeeks.org/lodash-_-isset-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

_ **。isSet()** 方法用于查找给定值是否归类为 Set 对象。如果给定值是一个集合，它返回真。否则，它返回 false。

**语法:**

```
_.isSet(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值为集合，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Creating a array of size 2 
var obj= new Array(2);

// Filling array with value 10 
obj.fill(10); 

// Use of _.isSet() method 
console.log(_.isSet(obj));
```

**输出:**

```
false
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isSet() method 
console.log(_.isSet(new Set)); 
console.log(_.isSet(new WeakSet)); 
```

**输出:**

```
true
false
```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。