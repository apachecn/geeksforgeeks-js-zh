# Collect.js join()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-join-method/](https://www.geeksforgeeks.org/collect-js-join-method/)

**join()方法**用于连接给定字符串的集合元素，并返回集合元素。

**语法:**

```
collect(array).join()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 join()方法。

**返回值:**该方法将集合元素与给定的字符串连接起来，并返回值。

下面的例子说明了 collect.js 中的 join()方法:

**例 1:**

```
const collect = require('collect.js');

let arr1 = [10, 20, 30, 40, 50];

const collection1 = collect(arr1);

console.log(collection1.join(', '));

let arr2 = ['a', 'b', 'c', 'd'];

const collection2 = collect(arr2);

console.log(collection2.join(', ', ' and '));
```

**输出:**

```
10, 20, 30, 40, 50
a, b, c and d

```

**例 2:**

```
const collect = require('collect.js');

let arr = ['Geeks', 'GFG', 'GeeksforGeeks'];

const collection = collect(arr);

console.log(collection.join(', '));
```

**输出:**

```
Geeks, GFG, GeeksforGeeks

```