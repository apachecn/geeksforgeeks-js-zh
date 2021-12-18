# Collect.js pop()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-pop-method/](https://www.geeksforgeeks.org/collect-js-pop-method/)

**pop()方法**用于从集合中移除最后一个元素，并返回弹出的元素。

**语法:**

```
collect(array).pop()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 pop()方法。

**返回值:**该方法返回给定集合中弹出的元素。

下面的例子说明了 collect.js 中的 pop()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 'GFG', 'GeeksforGeeks']);

console.log("Popped Elements: " + collection.pop());

console.log("Collection Elements: " + collection.all());
```

**输出:**

```
Popped Elements: GeeksforGeeks
Collection Elements: Geeks,GFG
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96'
    },
    {
        name: 'Aditya',
        dob: '25-10-96'
    },
    {
        name: 'Abhishek',
        dob: '16-08-94'
    }
];

const collection = collect(obj);

console.log("Popped Element");
console.log(collection.pop());

console.log("Collection Elements");
console.log(collection.all());
```

**输出:**

```
Popped Element
{ name: 'Abhishek', dob: '16-08-94' }
Collection Elements
[
  { name: 'Rahul', dob: '25-10-96' },
  { name: 'Aditya', dob: '25-10-96' }
]
```