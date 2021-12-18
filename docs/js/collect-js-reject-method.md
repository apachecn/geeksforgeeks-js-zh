# Collect.js reject()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-reject-method/](https://www.geeksforgeeks.org/collect-js-reject-method/)

**reject()方法**用于使用给定的回调函数过滤给定的元素集合。如果回调函数返回 true，则从结果集合中移除元素，否则不移除元素。

**语法:**

```
collect(array).reject(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 reject()方法。reject()方法将回调作为参数保存。

**返回值:**这个方法从集合中返回过滤后的元素。

下面的例子说明了 collect.js 中的 reject()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let obj = ['Geeks', 'GFG', 'GeeksforGeeks'];

const collection = collect(obj);

const filtered = collection.reject(
    element => element.length > 4);

console.log(filtered.all());
```

**输出:**

```
[ 'GFG' ]
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

const filtered = collection.reject(
    element => element.name.length > 5);

console.log(filtered.all());
```

**输出:**

```
[ { name: 'Rahul', marks: 88 } ]
```