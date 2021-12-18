# Collect.js sortByDesc()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sortbydesc-method/](https://www.geeksforgeeks.org/collect-js-sortbydesc-method/)

**sortByDesc()方法**用于根据给定的关键字将给定的集合元素按降序排序。

**语法:**

```
collect(array).sortByDesc(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sortByDesc()方法。sortByDesc()方法将键作为参数保存。

**返回值:**该方法根据给定的关键字将集合元素按降序返回。

下面的例子说明了 collect.js 中的 sortByDesc()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'Welcome', 'GFG', 'GeeksforGeeks']);

const sort_val = collection.sortByDesc();
console.log(sort_val);
```

**输出:**

```
Collection { items: [ 'Welcome', 'GeeksforGeeks', 'Geeks', 'GFG' ] }
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

const sort_val = collection.sortByDesc('name')
console.log(sort_val);
```

**输出:**

```
Collection {
  items: [
    { name: 'Rahul', marks: 88 },
    { name: 'Aditya', marks: 78 },
    { name: 'Abhishek', marks: 87 }
  ]
}
```