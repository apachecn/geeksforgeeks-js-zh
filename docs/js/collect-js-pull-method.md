# Collect.js 拉()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-pull-method/](https://www.geeksforgeeks.org/collect-js-pull-method/)

**拉()方法**用于通过给定的键从集合中移除一个元素，并返回被拉的元素。

**语法:**

```
collect(array).pull(key)
```

**参数:**collect()方法获取一个参数，该参数被转换为集合，然后对其应用 pull()方法。pull()方法将键作为参数保存。

**返回值:**该方法返回给定键的值。

下面的例子说明了 collect.js 中的 pull()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

let obj = ['Welcome', 'Geeks', 'GFG', 'GeeksforGeeks'];

const collection = collect(obj);

console.log(collection.pull(3));
```

**输出:**

```
GeeksforGeeks
```

**例二:**

## Javascript

```
const collect = require('collect.js');

let obj = {
    name: 'Rahul',
    dob: '25-10-96',
    section: 'A',
    score: 98,
};

const collection = collect(obj);

console.log(collection.pull('name'));
console.log(collection.pull('dob'));
```

**输出:**

```
Rahul
25-10-96
```