# Collect.js mapInto()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-mapinto-method/](https://www.geeksforgeeks.org/collect-js-mapinto-method/)

**mapInto()方法**用于迭代集合元素，并以每个元素作为构造函数实例化给定的类。

**语法:**

```
collect(array).mapInto()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 mapInto()方法。

**返回值:**此方法返回映射的集合元素。

下面的例子说明了 collect.js 中的 mapInto()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const data = function (name) {
    this.name = name;
};

const arr = ['GFG', 'Geeks', 'GeeksforGeeks'];

const collection = collect(arr);

const elements = collection.mapInto(data);

console.log(elements.all());
```

**输出:**

```
[
  data { name: 'GFG' },
  data { name: 'Geeks' },
  data { name: 'GeeksforGeeks' }
]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

const data = function (name, dob) {
    this.name = name;
    this.dob = dob;
};

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96',
        section: 'A',
        score: 98,
    },
    {
        name: 'Aditya',
        dob: '25-10-96',
        section: 'B',
        score: 96,
    },
    {
        name: 'Abhishek',
        dob: '16-08-94',
        section: 'A',
        score: 80
    },
    {
        name: 'Rahul',
        dob: '19-08-96',
        section: 'B',
        score: 77,
    },
];

const collection = collect(obj);

const objects = collection.mapInto(data);

console.log(objects.all());
```

**输出:**

```
[
  data {
    name: { 
      name: 'Rahul', 
      dob: '25-10-96', 
      section: 'A', 
      score: 98 
    },
    dob: 0
  },
  data {
    name: { 
      name: 'Aditya', 
      dob: '25-10-96', 
      section: 'B', 
      score: 96 },
    dob: 1
  },
  data {
    name: { 
      name: 'Abhishek', 
      dob: '16-08-94', 
      section: 'A', 
      score: 80 
    },
    dob: 2
  },
  data {
    name: { 
      name: 'Rahul', 
      dob: '19-08-96', 
      section: 'B', 
      score: 77 
    },
    dob: 3
  }
]
```