# Collect.js shuffle()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-shuffle-method/](https://www.geeksforgeeks.org/collect-js-shuffle-method/)

shuffle()方法用于随机返回集合元素。

**语法:**

```
collect(array).shuffle()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 shuffle()方法。

**返回值:**该方法返回集合中随机出现的元素。

下面的例子说明了 collect.js 中的 shuffle()方法:

**例 1:**

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const shuffled = collection.shuffle();

console.log(shuffled.all());
```

**输出:**

```
[ 'Welcome', 'GFG', 'GeeksforGeeks', 'Geeks' ]
```

**例 2:**

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

const shuffled = collection.shuffle();

console.log(shuffled.all());
```

**输出:**

```
[
  { name: 'Rahul', marks: 88 },
  { name: 'Abhishek', marks: 87 },
  { name: 'Aditya', marks: 78 }
]
```