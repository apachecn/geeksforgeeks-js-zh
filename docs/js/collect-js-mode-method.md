# Collect.js 模式()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-mode-method/](https://www.geeksforgeeks.org/collect-js-mode-method/)

collect.js 的**模式()方法**用于返回给定按键的模式。模式是在一组观察中最频繁出现的值。

**语法:**

```
collect(array).mode(key)
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 mode()方法。mode()方法将键作为参数保存。

**返回值:**该方法从集合中返回给定键的模式。

下面的例子说明了 collect.js 中的 mode()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let arr = [1, 1, 3, 3, 3, 5, 5, 6];

const collection = collect(arr);

const mode_val = collection.mode();

console.log(mode_val);
```

**输出:**

```
3
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
        score: 98
    }
];

const collection = collect(obj);

const mode_val = collection.mode('score');

console.log(mode_val);
```

**输出:**

```
98
```