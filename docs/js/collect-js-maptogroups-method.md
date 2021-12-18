# Collect.js mapToGroups()方法

> 原文:[https://www . geesforgeks . org/collect-js-maptogroups-method/](https://www.geeksforgeeks.org/collect-js-maptogroups-method/)

**mapToGroups()方法**用于迭代集合元素，并将集合的每个值传递给给定的回调函数。

**语法:**

```
collect(array).mapToGroups(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 mapToGroups()方法。mapToGroups()方法将回调函数作为参数保存。

**返回值:**该方法根据给定的回调返回集合元素。

下面的例子说明了 collect.js 中的 mapToGroups()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [{
    name: 'Ashok',
    score: 75
},
{
    name: 'Rakesh',
    score: 86
},
{
    name: 'Rajesh',
    score: 56
},
{
    name: 'Rakesh',
    score: 98
}];

const collection = collect(obj);

const sequence = collection.mapToGroups(
    (element) => [element.name, element.score])

console.log(sequence.all());
```

**输出:**

```
{ Ashok: [ 75 ], Rakesh: [ 86, 98 ], Rajesh: [ 56 ] }
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96',
    },
    {
        name: 'Aditya',
        dob: '25-10-96',
    },
    {
        name: 'Abhishek',
        dob: '16-08-94',
    },
    {
        name: 'Rahul',
        dob: '25-10-96',
    },
];

const collection = collect(obj);

const sequence = collection.mapToGroups(
    (element) => [element.dob, element.name])

console.log(sequence.all());
```

**输出:**

```
{
  '25-10-96': [ 'Rahul', 'Aditya', 'Rahul' ],
  '16-08-94': [ 'Abhishek' ]
}
```