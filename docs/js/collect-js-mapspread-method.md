# Collect.js mapSpread()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-mapspread-method/](https://www.geeksforgeeks.org/collect-js-mapspread-method/)

**mapSpread()方法**用于迭代给定的集合项，并将每个嵌套的集合项值传递给给定的回调。

**语法:**

```
collect(array).mapSpread(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 mapSpread()方法。mapSpread()方法将回调函数作为参数保存。

**返回值:**该方法根据给定的回调函数返回集合项。

下面的例子说明了 collect.js 中的 mapSpread()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

const arr = ['a', 'b', 'c'];

const collection = collect(arr);

const sequence = collection.mapSpread(
    element => element.toUpperCase());

console.log(sequence.all());
```

**输出:**

```
[ 'A', 'B', 'C' ]
```

**例二:**

## Javascript

```
const collect = require('collect.js');

const arr = [2, 4, 5, 6, 7, 8, 10, 11];

const collection = collect(arr);

const sequence = collection.mapSpread(
    element => element % 2 == 0);

console.log(sequence.all());
```

**输出:**

```
[
  true, false,
  true, false,
  true, false,
  true, false
]
```