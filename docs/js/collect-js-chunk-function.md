# Collect.js | chunk()函数

> 原文:[https://www.geeksforgeeks.org/collect-js-chunk-function/](https://www.geeksforgeeks.org/collect-js-chunk-function/)

**chunk()函数**将集合分解成许多给定大小的小集合。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.chunk(x)

```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **x :** 此参数保存一个整数，用于定义在何处中断集合

**返回值:**返回主集合的子集合

下面的例子说明了 collect.js:
**中的 **chunk()** 函数示例 1:** 在本例中，我们取一个集合，然后使用 **chunk()** 函数对集合进行划分。

## java 描述语言

```
// It is used to import collect.js library

const collect = require('collect.js');

const collection = collect([1, 2, 3, 4, 5, 6, 7]);

const x = collection.chunk(5);

console.log(x.all());
```

**输出:**

```
[ Collection { items: [ 1, 2, 3, 4, 5 ] },
  Collection { items: [ 6, 7 ] } ]

```

**示例 2:** 在本例中，我们将在**组块()函数**中传递两个值。

## java 描述语言

```
// It is used to import collect.js library

const collect = require('collect.js');

const collection = collect([0 , 1 , 2 , 3 , 4 , 5 , 6 ]);

const x = collection.chunk(2, 4);

console.log(x.all());
```

**输出:**

```
[ Collection { items: [ 0, 1 ] },
  Collection { items: [ 2, 3 ] },
  Collection { items: [ 4, 5 ] },
  Collection { items: [ 6 ] } ]

```