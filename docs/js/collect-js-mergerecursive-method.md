# Collect.js mergeRecursive()方法

> 原文:[https://www . geesforgeks . org/collect-js-merge recursive-method/](https://www.geeksforgeeks.org/collect-js-mergerecursive-method/)

**mergeRecursive()方法**用于将给定的数组或集合元素与原始集合递归合并。当第一个集合元素的键与第二个集合的键匹配时，这些键的值被递归地合并到一个数组中。

**语法:**

```
collect(array).mergeRecursive(object)
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 mergeRecursive()方法。它将对象或集合作为参数保存。

**返回值:**该方法返回合并后的集合元素。

下面的例子说明了 collect.js 中的 mergeRecursive()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

let obj = ['Geeks', 'GeeksforGeeks'];

const collection = collect(obj);

const merged_val = collection
    .mergeRecursive(['Welcome', 'GFG']);

console.log(merged_val.all());
```

**输出:**

```
{ '0': [ 'Geeks', 'Welcome' ], '1': [ 'GeeksforGeeks', 'GFG' ] }
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
    }
];

const collection = collect(obj);

const merged_val = collection.mergeRecursive({
    address: 'Noida',
    school: 'GeeksforGeeks',
});

console.log(merged_val.all());
```

**输出:**

```
{
  '0': { name: 'Rahul', dob: '25-10-96' },
  '1': { name: 'Aditya', dob: '25-10-96' },
  address: 'Noida',
  school: 'GeeksforGeeks'
}
```