# Collect.js 次()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-times-method/](https://www.geeksforgeeks.org/collect-js-times-method/)

**times()方法**用于通过调用回调给定次数来创建新集合。

**语法:**

```
collect.times()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 times()方法。

**返回值:**这个方法通过调用回调给定次数来返回一个新的集合。

下面的例子说明了 collect.js 中的 times()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js'); 

const collection = collect()
    .times(8, number => number + 5);

let newObject = collection.all();

console.log(newObject);
```

**输出:**

```
[6, 7, 8, 9, 10, 11, 12, 13]
```

**例二:**

## Javascript

```
const collect = require('collect.js'); 

const collection = collect()
    .times(8, number => number * 5);

let newObject = collection.all();

console.log(newObject);
```

**输出:**

```
[5, 10, 15, 20, 25, 30, 35, 40]
```