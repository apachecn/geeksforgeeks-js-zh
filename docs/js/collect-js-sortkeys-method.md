# Collect.js sortKeys()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sortkeys-method/](https://www.geeksforgeeks.org/collect-js-sortkeys-method/)

**sortKeys()方法**用于根据底层关联数组的给定键对集合元素进行排序。

**语法:**

```
collect(array).sortKeys(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sortKeys()方法。sortKeys()方法将键作为参数保存。

**返回值:**这个方法返回集合元素按底层关联数组的给定键排序。

下面的例子说明了 collect.js 中的 sortKeys()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let obj = ({
    name: 'Rahul',
    dob: '25-10-96',
    section: 'A',
    score: 98
});

const collection = collect(obj);

const sorted = collection.sortKeys();

console.log(sorted.all());
```

**输出:**

```
{ dob: '25-10-96', name: 'Rahul', score: 98, section: 'A' }
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = ({
    5: "Welcome",
    1: "GeeksforGeeks",
    8: "to",
    4: "Computer",
    9: "Science",
    10: "Portal"
});

const collection = collect(obj);

const sorted = collection.sortKeys();

console.log(sorted.all());
```

**输出:**

```
{
  '1': 'GeeksforGeeks',
  '4': 'Computer',
  '5': 'Welcome',
  '8': 'to',
  '9': 'Science',
  '10': 'Portal'
}
```