# 洛达什 _。合并()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-merge-method/](https://www.geeksforgeeks.org/lodash-_-merge-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。merge()** 方法用于从最左边到最右边合并两个或多个对象，以创建父映射对象。当两个键相同时，生成的对象将具有最右边键的值。如果多个对象相同，新生成的对象将只有一个对应于这些对象的键和值。

**语法:**

```
_.merge( object, sources )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存目标对象。
*   **来源:**此参数保存来源对象。这是一个可选参数。

**返回值:**该方法返回合并后的对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Using the _.merge() method 
console.log(
  _.merge({ cpp: "12" }, { java: "23" },
          { python:"35" })
 );

// When two keys are the same
console.log(
  _.merge({ cpp: "12" }, { cpp: "23" },
          { java: "23" }, { python:"35" })
);

// When more than one object is the same
console.log(
  _.merge({ cpp: "12" }, { cpp: "12" },
          { java: "23" }, { python:"35" })
);
```

**输出:**

```
{cpp: '12', java: '23', python: '35'}
{cpp: '23', java: '23', python: '35'}
{cpp: '12', java: '23', python: '35'}

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The destination object
var object = {
  'amit': [{ 'susanta': 20 }, { 'durgam': 40 }]
};

// The source object
var other = {
  'amit': [{ 'chinmoy': 30 }, { 'kripamoy': 50 }]
};

// Using the _.merge() method
console.log(_.merge(object, other));
```

**输出:**

```
{ 'amit': [{'chinmoy': 30, 'susanta': 20 }, 
{ 'durgam': 40, 'kripamoy': 50 }] }

```