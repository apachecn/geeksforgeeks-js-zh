# Collect.js union()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-union-method/](https://www.geeksforgeeks.org/collect-js-union-method/)

**union()方法**用于将给定的数组添加到具有唯一值的集合中。如果给定数组包含原始集合中已有的值，则首选原始集合的值。

**语法:**

```
collect.union()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 union()方法。

**返回值:**该方法返回具有唯一元素的集合。

下面的例子说明了 collect.js 中的 union()方法:

**例 1:**

```
const collect = require('collect.js'); 

let obj = [1, 2, 3, 4, 5]; 

const collection = collect(obj); 

const union = collection.union([1, 2, 3, 2, 4]); 

console.log(union.all());
```

**输出:**

```
[1, 2, 3, 4, 5]
```

**例 2:**

```
const collect = require('collect.js');

let obj = ({
    name1: 'AAA',
    name2: 'BBB',
});

const collection = collect(obj);

const union = collection.union({
    name1: 'AAAAA',
    name3: 'CCCCC',
    name2: 'BBBBB',
});

console.log(union.all());
```

**输出:**

```
{name1: "AAA", name2: "BBB", name3: "CCCCC"}
```