# Collect.js min()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-min-method/](https://www.geeksforgeeks.org/collect-js-min-method/)

**min()方法**用于从给定的数组或集合中返回最小元素。可以用一个键作为参数来指定方法，以便只考虑集合中该键的值，并从这些值中找到最小元素。

**语法:**

```
collect(array).min(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 min()方法。min()方法将键作为参数保存。

**返回值:**该方法返回给定集合中的最小元素。

下面的例子说明了 collect.js 中的 min()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let arr = [10, 15, -20, -25, 40, 50, -70];

const collection = collect(arr);

const min_val = collection.min();

console.log(min_val);
```

**输出:**

```
-70
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96',
        section: 'A',
        score: 98,
    },
    {
        name: 'Aditya',
        dob: '25-10-96',
        section: 'B',
        score: 96,
    },
    {
        name: 'Abhishek',
        dob: '16-08-94',
        section: 'A',
        score: 80
    }
];

const collection = collect(obj);

const min_score = collection.min('score');

console.log(min_score);
```

**输出:**

```
80
```