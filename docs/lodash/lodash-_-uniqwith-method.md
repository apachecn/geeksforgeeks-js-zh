# 洛达什 _。uniqWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-uniqwith-method/](https://www.geeksforgeeks.org/lodash-_-uniqwith-method/)

**_。uniqWith()方法**类似于 _。uniq()方法(即它创建一个数组的无重复版本，其中只保留每个元素的第一次出现。)除了它接受比较器，该比较器被调用来比较数组的元素。结果值的顺序由它们在数组中出现的顺序决定。

**语法:**

```
_.uniqWith(array, [comparator])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be checked.
*   **[Comparator] (function):** This parameter holds the comparator called by each element and is called with two parameters (arrVal and othVal).

**返回值:**该方法返回新的无重复数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var objects = [{ 'x': 5, 'y': 2 }, { 'x': 3, 'y': 

4 }, { 'x': 5, 'y': 2 } ];    

// Use of _.uniqWith() method
let gfg = _.uniqWith(objects, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ { x: 5, y: 2 }, { x: 3, y: 4 } ]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var objects = [ 2.2, 3.2, 4.2, 3.2, 5.2, 4.2 ];    

// Use of _.uniqWith() method
let gfg = _.uniqWith(objects, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[ 2.2, 3.2, 4.2, 5.2]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var objects = ['p', 'q', 'r', 
      'u', 's', 't', 'r', 'u'];    

// Use of _.uniqWith() method
let gfg = _.uniqWith(objects, _.isEqual);

// Printing the output 
console.log(gfg);
```

**输出:**

```
['p', 'q', 'r', 'u', 's', 't']

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。