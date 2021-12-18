# 洛达什 _。isWeakMap()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isweakmap-method/](https://www.geeksforgeeks.org/lodash-_-isweakmap-method/)

**_。iswakmap()****方法**用于查找给定值是否为 WeakMap 对象。如果给定值是 weakmap 对象，则返回 True。否则，它返回 false。

**语法:**

```
_.isWeakMap(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值是武器，该方法返回真，否则返回假。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

```
// Requiring the lodash library  
const _ = require("lodash");  

// Creating a array of size 2
// using constructor 
var obj= new Array(2); 

// Filling value 5 in the array 
obj.fill(5) 

// Use of _.isWeakMap() method 
console.log(_.isWeakMap(obj)); 
```

**输出:**

```
false

```

**例 2:**

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isWeakMap() method 

// When a weak set is given
console.log(_.isWeakMap(new WeakMap)); 

// When a weak set is not given
console.log(_.isWeakMap(new Map));
```

**输出:**

```
true
false

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考资料:**[https://lodash . com/docs/4 . 17 . 15 # is weak map](https://lodash.com/docs/4.17.15#isWeakMap)