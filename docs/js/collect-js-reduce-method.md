# Collect.js reduce()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-reduce-method/](https://www.geeksforgeeks.org/collect-js-reduce-method/)

**reduce()方法**用于根据给定的回调将集合元素缩减为单个值。它的工作原理是将每次迭代的结果传递给下一次迭代，最终得到一个值。

**语法:**

```
collect(array).reduce(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 reduce()方法。reduce()方法将回调函数作为参数保存。

**返回值:**此方法返回集合的缩减值。

下面的例子说明了 collect.js 中的 reduce()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let obj = ['Geeks', 'GFG', 'GeeksforGeeks'];

const collection = collect(obj);

const total_string_len =
  collection.reduce(
  (str_len, element) => 
    str_len + element.length);

console.log(total_string_len);
```

**输出:**

```
21
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

const total_name_len =
  collection.reduce(
    (str_len, element) => 
    str_len + element.name.length);

console.log(total_name_len);

const total_marks = collection.reduce(
    (marks, element) =>
     marks + element.marks);

console.log(total_marks);
```

**输出:**

```
19
253
```