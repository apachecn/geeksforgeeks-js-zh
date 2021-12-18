# Collect.js 除外()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-except-method/](https://www.geeksforgeeks.org/collect-js-except-method/)

**除()方法**用于返回给定集合中除指定键以外的所有项。

**语法:**

```
collect(array).except(key)

```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 except()方法。except()方法将一个参数作为要从给定集合中移除的键。

**返回值:**此方法返回除给定关键字项以外的集合项。

下面的例子说明了 collect.js 中的 except()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

const arr = [2, 4, 5, 6, 8, 9, 10];

const collection = collect(arr);

const remaining_element = 
    collection.except(5, 7, 9, 10, 12);

console.log(remaining_element);
```

**输出:**

```
Collection { items: [ 2, 4, 6, 8 ] }

```

**例二:**

## Javascript

```
const collect = require('collect.js');

const arr = ['Geeks', 'GFG', 'GeeksforGeeks', 'Welcome'];

const collection = collect(arr);

const remaining_element = collection.except('GFG');

console.log(remaining_element);
```

**输出:**

```
Collection { items: [ 'Geeks', 'GeeksforGeeks', 'Welcome' ] }

```