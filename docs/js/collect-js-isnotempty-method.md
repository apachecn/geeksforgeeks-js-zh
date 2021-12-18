# Collect.js isNotEmpty()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-isnotempty-method/](https://www.geeksforgeeks.org/collect-js-isnotempty-method/)

**isNotEmpty()方法**用于检查给定集合是否为空，并返回相应的布尔值。如果集合不为空，则返回 true，否则返回 false。

**语法:**

```
collect(array).isNotEmpty()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 isNotEmpty()方法。

**返回值:**该方法检查给定集合是否为空，并返回相应的布尔值。

下面的例子说明了 collect.js 中的 isNotEmpty()方法:

**例 1:**

```
const collect = require('collect.js');

let arr = [];

const collection = collect(arr);

const isemp = collection.isNotEmpty();

console.log(isemp);
```

**输出:**

```
false
```

**例 2:**

```
const collect = require('collect.js');

const collection = collect({});

const isemp1 = collection.isNotEmpty();

console.log(isemp1);

const collection1 = collect([10, 20, 30]);

const isemp2 = collection1.isNotEmpty();

console.log(isemp2);
```

**输出:**

```
false
true

```