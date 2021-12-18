# 采集. js 值()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-values-method/](https://www.geeksforgeeks.org/collect-js-values-method/)

**values()方法**用于返回一个新的集合，给定的键被重置为连续的整数。

**语法:**

```
collect(array).values(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 values()方法。values()方法将键作为参数保存。

**返回值:**这个方法返回一个新的集合，给定的键被重置为连续的整数。

下面的例子说明了 collect.js 中的 values()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks',
    'Welcome', 'GFG', 'GeeksforGeeks']);

const val = collection.values();

console.log(val.all());
```

**输出:**

```
[ 'Geeks', 'Welcome', 'GFG', 'GeeksforGeeks' ]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        marks: 88
    },
    {
        name: 'Aditya',
        marks: 78
    },
    {
        name: 'Abhishek',
        marks: 87
    }
];

const collection = collect(obj);

const val = collection.values();

console.log(val.all());
```

**输出:**

```
[
  { name: 'Rahul', marks: 88 },
  { name: 'Aditya', marks: 78 },
  { name: 'Abhishek', marks: 87 }
]
```