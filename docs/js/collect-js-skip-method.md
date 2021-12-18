# Collect.js skip()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-skip-method/](https://www.geeksforgeeks.org/collect-js-skip-method/)

**skip()方法**用于从集合中跳过给定数量的元素，并返回剩余的集合元素。

**语法:**

```
collect(array).skip(size)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 skip()方法。skip()方法将大小(要从集合中跳过的元素数量)作为参数。

**返回值:**该方法返回剩余的集合元素。

下面的例子说明了 collect.js 中的 skip()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const skipped = collection.skip(2);

console.log(skipped.all());
```

**输出:**

```
[ 'GeeksforGeeks', 'Welcome' ]
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

const skipped = collection.skip(1);

console.log(skipped.all());
```

**输出:**

```
[ { name: 'Aditya', marks: 78 }, { name: 'Abhishek', marks: 87 } ]
```