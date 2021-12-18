# collect . js intersecbykeys()方法

> 原文:[https://www . geesforgeks . org/collect-js-intersecbykeys-method/](https://www.geeksforgeeks.org/collect-js-intersectbykeys-method/)

**intersecbykeys()方法**用于从原始集合中移除给定数组或集合中不存在的任何给定键。

**语法:**

```
collection.intersectByKeys(key)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **键:**此参数保存需要从原始集合相交的键或键、值对。

**返回值:**该方法返回相交的集合项。

下面的例子说明了 collect.js 中的 intersectByKeys()方法:

**例 1:**

```
const collect = require('collect.js');

const collection = collect({
    name: 'Rahul',
    class: 'IX',
    section: 'A',
    score: 98
});

const intersect_val = collection.intersectByKeys({
    name: 'Rakesh',
    age: 24,
    section: 'B',
    year: 2011
});

console.log(intersect_val.all());
```

**输出:**

```
{ name: 'Rahul', section: 'A' }
```

**例 2:**

```
const collect = require('collect.js');

const collection1 = collect({
    key11: 'val1',
    key12: 'val2',
    key13: 'val3'
});

const collection2 = collect({
    key11: 'val1',
    key22: 'val2',
    key13: 'val3'
});

const intersect_val = 
collection1.intersectByKeys(collection2);

console.log(intersect_val.all());
```

**输出:**

```
{ key11: 'val1', key13: 'val3' }
```