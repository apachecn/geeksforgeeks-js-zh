# Collect.js sortDesc()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sortdesc-method/](https://www.geeksforgeeks.org/collect-js-sortdesc-method/)

**sortDesc()方法**用于按照与排序方法相反的顺序对集合进行排序。

**语法:**

```
collect.sortDesc()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sortDesc()方法。

**返回值:**该方法按降序返回集合。

下面的例子说明了 collect.js 中的 sortDesc()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let arr = [8, 4, 7, 6, 5, 11, 3];

const collection = collect(arr);

const sorted = collection.sortDesc();

let result = sorted.all();

console.log(result);
```

**输出:**

```
[11, 8, 7, 6, 5, 4, 3]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        subject: 'English',
        score: 95,
    },
   {
        subject: 'math',
        score: 86,
    },
    {
        subject: 'science',
        score: 90,
    }
];

const collection = collect(obj);

const sorted = collection.sortDesc('score');

let result = sorted.all();

console.log(result);
```

**输出:**

```
 [ 
   { 
        subject: 'science', 
        score: 90, 
   },
   { 
        subject: 'English', 
        score: 95, 
   },
      { 
        subject: 'math', 
        score: 86, 
   }
]
```