# Collect.js skipWhile()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-skipwhile-method/](https://www.geeksforgeeks.org/collect-js-skipwhile-method/)

skipWhile()方法用于跳过集合元素，而给定的回调函数返回 true 并返回剩余的集合元素。

**语法:**

```
collect(array).skipWhile(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 skipWhile()方法。skipWhile()方法将回调作为参数保存。

**返回值:**该方法返回剩余的集合元素。

下面的例子说明了 collect.js 中的 skipWhile()方法:

**例 1:**

```
const collect = require('collect.js');

const collection = collect([10, 22, 24, 28, 34, 36, 39]);

const skipWhile_val = collection
    .skipWhile(element => element % 5 == 0);

console.log(skipWhile_val.all());
```

**输出:**

```
[ 22, 24, 28, 34, 36, 39 ]
```

**例 2:**

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

const skipWhile_val = collection.skipWhile(
    element => element.name.length == 5);

console.log(skipWhile_val.all());
```

**输出:**

```
[ { name: 'Aditya', marks: 78 }, { name: 'Abhishek', marks: 87 } ]
```