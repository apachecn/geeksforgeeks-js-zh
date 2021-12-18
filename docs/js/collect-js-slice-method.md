# Collect.js 切片()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-slice-method/](https://www.geeksforgeeks.org/collect-js-slice-method/)

**切片()方法**用于从给定索引开始返回给定集合的切片。

**语法:**

```
collect(array).slice(size)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 slice()方法。slice()方法将大小保存为参数。

**返回值:**这个方法从给定的索引开始返回给定集合的一个切片。

下面的例子说明了 collect.js 中的 slice()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

const collection = collect([10, 22, 24, 28, 34, 36, 39]);

const slice_val = collection.slice(3);

console.log(slice_val.all());
```

**输出:**

```
[ 28, 34, 36, 39 ]
```

**例二:**

## Javascript

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const slice_val = collection.slice(2, 2);

console.log(slice_val.all());
```

**输出:**

```
[ 'GeeksforGeeks', 'Welcome' ]
```