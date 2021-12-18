# 洛达什 _。mapKeys()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mapkeys-method/](https://www.geeksforgeeks.org/lodash-_-mapkeys-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。mapKeys()** 方法用于创建一个对象，该对象具有与对象相同的值，并且通过运行每个对象自己的可枚举字符串键来创建键。

**语法:**

```
_.mapKeys( object, iteratee )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存要迭代的对象。
*   **迭代:**是每次迭代调用的函数。

**返回值:**该方法返回新的映射对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");

// Using the _.mapKeys() method 
console.log(
  _.mapKeys({ 'cpp': 15, 'java': 40, 'python': 63 },
      function(value, key) {
          return  key + value ;
  }
));
```

**输出:**

```
{'cpp15': 15, 'java40': 40, 'python63': 63}

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var info = {
  'GFG': { 'user': 'amit', 'age': 23 },
  'codechef': { 'user': 'priya', 'age': 21 }
};

// Using the _.mapKeys() method 
console.log(_.mapKeys(info,
  function(o) { return o.age; })
);
```

**输出:**

```
{21: {'age': 21, 'user': "priya"}, 23: {'age': 23, 'user': "amit"}}

```