# Collect.js 按键()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-keys-method/](https://www.geeksforgeeks.org/collect-js-keys-method/)

**键()方法**用于返回集合的所有键。

**语法:**

```
collect(array).keys()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 keys()方法。

**返回值:**此方法返回集合键。

下面的例子说明了 collect.js 中的 key()方法:

**例 1:**

```
const collect = require('collect.js');

const collection = collect({
    name: 'Rahul',
    dob: '25-10-96',
    section: 'A',
    score: 98,
});

const keys_val = collection.keys();

console.log(keys_val.all());
```

**输出:**

```
[ 'name', 'dob', 'section', 'score' ]
```

**例 2:**

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
    },
    {
        name: 'Rahul',
        dob: '19-08-96',
        section: 'B',
        score: 77,
    },
];

const collection = collect(obj);

const keys_val = collection.keys();

console.log(keys_val.all());
```

**输出:**

```
[ 0, 1, 2, 3 ]

```