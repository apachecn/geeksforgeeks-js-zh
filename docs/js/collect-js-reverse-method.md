# Collect.js 反向()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-reverse-method/](https://www.geeksforgeeks.org/collect-js-reverse-method/)

**反转()方法**用于反转给定集合的顺序。它可以用来反转元素或嵌套对象的数组。

**语法:**

```
collect(array).reverse()
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 reverse()方法。

**返回值:**此方法以相反的顺序返回集合元素。

下面的例子说明了 collect.js 中的 reverse()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(
    ['Geeks', 'GFG', 'GeeksforGeeks']);

const reversed = collection.reverse();

console.log(reversed.all());
```

**输出:**

```
[ 'GeeksforGeeks', 'GFG', 'Geeks' ]
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

const reversed = collection.reverse();

console.log(reversed.all());
```

**输出:**

```
[
  { name: 'Abhishek', marks: 87 },
  { name: 'Aditya', marks: 78 },
  { name: 'Rahul', marks: 88 }
]
```