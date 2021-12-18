# Collect.js mapToDictionary()方法

> 原文:[https://www . geesforgeks . org/collect-js-maptodictionary-method/](https://www.geeksforgeeks.org/collect-js-maptodictionary-method/)

**mapToDictionary()方法**用于在集合项上运行字典映射。给定的回调函数返回具有单个(键、值)对的关联数组。

**语法:**

```
collect(array).mapToDictionary(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 mapToDictionary()方法。mapToDictionary()方法将回调函数作为参数保存。

**返回值:**这个方法返回一个具有单个(键，值)对的关联数组。

下面的例子说明了 collect.js 中的 mapToDictionary()方法:

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
}];

const collection = collect(obj);

const sequence = collection.mapToDictionary(
    element => [element.name, element.score]);

console.log(sequence.all());
```

**输出:**

```
{ Ashok: [ 75 ], Rakesh: [ 86 ], Rajesh: [ 56 ] }
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
        dob: '19-08-96',
    },
];

const collection = collect(obj);

const sequence = collection.mapToDictionary(
    element => [element.name, element.dob]);

console.log(sequence.all());
```

**输出:**

```
{
  Rahul: [ '25-10-96', '19-08-96' ],
  Aditya: [ '25-10-96' ],
  Abhishek: [ '16-08-94' ]
}
```