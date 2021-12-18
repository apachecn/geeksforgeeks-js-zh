# 采集. js 采摘()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-pluck-method/](https://www.geeksforgeeks.org/collect-js-pluck-method/)

**pull()方法**用于返回给定键的所有值。

**语法:**

```
collect(array).pluck(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 pluck()方法。pluck()方法将键作为参数保存。

**返回值:**该方法返回给定键的所有值。

下面的例子说明了 collect.js 中的 purge()方法:

**例 1:**

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

const pluck_val = collection.pluck('name');

console.log(pluck_val.all());
```

**输出:**

```
[ 'Rahul', 'Aditya', 'Abhishek' ]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96'
    },
    {
        name: 'Aditya',
        dob: '25-10-96'
    },
    {
        name: 'Abhishek',
        dob: '16-08-94'
    }
];

const collection = collect(obj);

const pluck_val = collection.pluck('name', 'dob');

console.log(pluck_val.all());
```

**输出:**

```
{ '25-10-96': 'Aditya', '16-08-94': 'Abhishek' }
```