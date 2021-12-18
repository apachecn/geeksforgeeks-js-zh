# Collect.js 过滤器()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-filter-method/](https://www.geeksforgeeks.org/collect-js-filter-method/)

**filter()方法**用于使用给定的回调函数过滤给定的集合，并返回集合元素。

**语法:**

```
collect(array).filter(callback)

```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 filter()方法。filter()方法接受一个保存回调函数值的参数。

**返回值:**该方法返回过滤后的集合元素。

下面的例子说明了 collect.js 中的 filter()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const arr = [2, 4, 5, 6, 8, 9, 10];

const collection = collect(arr);

const remaining_element = collection
    .filter((val, key) => val % 2 == 0);

console.log(remaining_element.all());
```

**输出:**

```
[ 2, 4, 6, 8, 10 ]

```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        score: 98,
    },
    {
        name: 'Aditya',
        score: 96,
    },
    {
        name: 'Abhishek',
        score: 80
    },
];

const collection = collect(obj);

const remaining_element = collection
    .filter((val, key) => val.score > 80);

console.log(remaining_element.all());
```

**输出:**

```
[ 
    { name: 'Rahul', score: 98 }, 
    { name: 'Aditya', score: 96 } 
]

```