# Collect.js firstWhere()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-firstwhere-method/](https://www.geeksforgeeks.org/collect-js-firstwhere-method/)

**firstWhere()方法**用于返回具有给定键和值对的集合中的第一个元素。通过仅指定对象中的任何键-值对，可以使用它来查找数组中的任何元素。

**语法:**

```
collect(array).firstWhere( key, value )

```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 firstWhere()方法。firstWhere()方法将要搜索的键和值对作为参数。

**返回值:**返回集合中给定键和值对的第一个元素。

下面的例子说明了 collect.js 中的 **firstWhere()方法**:

**例 1:**

## java 描述语言

```
const collect = require("collect.js");

let obj = [
  {
    name: "Rahul",
    score: 98,
  },
  {
    name: "Aditya",
    score: 96,
  },
  {
    name: "Abhishek",
    score: 80,
  },
  {
    name: "Rahul",
    score: 77,
  },
];

const collection = collect(obj);

let first_Val = 
  collection.firstWhere("name", "Rahul");
console.log(first_Val);
```

**输出:**

```
{ name: 'Rahul', score: 98 }

```

**例 2:**

## java 描述语言

```
const collect = require("collect.js");

let obj = [
  {
    name: "Rahul",
    dob: "25-10-96",
    section: "A",
    score: 98,
  },
  {
    name: "Aditya",
    dob: "25-10-96",
    section: "B",
    score: 96,
  },
  {
    name: "Abhishek",
    dob: "16-08-94",
    section: "A",
    score: 80,
  },
  {
    name: "Rahul",
    dob: "19-08-96",
    section: "B",
    score: 77,
  },
];

const collection = collect(obj);

let first_Val = 
  collection.firstWhere("dob", "25-10-96");
console.log(first_Val);
```

**输出:**

```
{ name: 'Rahul', dob: '25-10-96', section: 'A', score: 98 }

```