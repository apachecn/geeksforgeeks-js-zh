# 收集一些()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-some-method/](https://www.geeksforgeeks.org/collect-js-some-method/)

**some()方法**用于检查给定集合是否包含给定项目，并返回相应的布尔值。

**语法:**

```
collect(array).some(key/value)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用一些()方法。some()方法将键/值作为参数保存。

**返回值:**该方法检查给定集合是否包含给定项，并返回相应的布尔值。

下面的例子说明了 collect.js 中的 some()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const some_val = collection.some('GFG');

console.log(some_val);
```

**输出:**

```
true
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

const some_val1 = collection.some(
    element => element.name == 'Aditya');
console.log(some_val1);

const some_val2 = collection.some(
    element => element.name == 'Shyam');
console.log(some_val2);
```

**输出:**

```
true
false
```