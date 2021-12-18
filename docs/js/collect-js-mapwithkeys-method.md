# Collect.js mapWithKeys()方法

> 原文:[https://www . geeksforgeeks . org/collect-js-mapwithkeys-method/](https://www.geeksforgeeks.org/collect-js-mapwithkeys-method/)

**mapWithKeys()方法**用于遍历集合元素，并将每个集合元素传递给给定的回调函数。回调函数返回一个包含键和值对的数组。

**语法:**

```
collect(array).mapWithKeys(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 mapWithKeys()方法。mapWithKeys()方法将回调函数作为参数保存。

**返回值:**这个方法返回一个包含键值对的数组。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 mapWithKeys()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
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

// Creating collection object
const collection = collect(obj);

// Function call
const sequence = collection.mapWithKeys(
    element => [element.name, element.dob]);

// Printing the sequence
console.log(sequence.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{ Rahul: '25-10-96', Aditya: '25-10-96', Abhishek: '16-08-94' }
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

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
    }
];

// Creating collection object
const collection = collect(obj);

// Function call
const sequence = collection.mapWithKeys(
    element => [element.name, element.section]);

// Printing the sequence
console.log(sequence.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{ Rahul: 'A', Aditya: 'B', Abhishek: 'A' }
```