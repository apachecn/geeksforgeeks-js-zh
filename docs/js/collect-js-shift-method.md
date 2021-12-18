# Collect.js shift()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-shift-method/](https://www.geeksforgeeks.org/collect-js-shift-method/)

**shift()方法**用于从集合中移除第一个元素并将其返回。

**语法:**

```
collect(array).shift()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 shift()方法。

**返回值:**这个方法返回给定集合的第一个元素。

下面的例子说明了 collect.js 中的 shift()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const shifted = collection.shift();

console.log(shifted);

console.log(collection.all());
```

**输出:**

```
Geeks
[ 'GFG', 'GeeksforGeeks', 'Welcome' ]
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

const shifted = collection.shift();

console.log(shifted);

console.log(collection.all());
```

**输出:**

```
{ name: 'Rahul', marks: 88 }
[ 
    { name: 'Aditya', marks: 78 }, 
    { name: 'Abhishek', marks: 87 } 
]
```