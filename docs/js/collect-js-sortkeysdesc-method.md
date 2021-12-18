# Collect.js sortKeysDesc()方法

> 原文:[https://www . geesforgeks . org/collect-js-sortkeysdesc-method/](https://www.geeksforgeeks.org/collect-js-sortkeysdesc-method/)

**sortKeysDesc()方法**用于根据底层关联数组的给定键对集合元素进行降序排序。

**语法:**

```
collect(array).sortKeysDesc(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sortKeysDesc()方法。sortKeysDesc()方法将键作为参数保存。

**返回值:**该方法按降序返回排序后的集合元素。

下面的例子说明了 collect.js 中的 sortKeysDesc()方法:

**例 1:**

## java 描述语言

```
const collect = require("collect.js");

let obj = {
  name: "Rahul",
  dob: "25-10-96",
  section: "A",
  score: 98,
};

const collection = collect(obj);

const sorted = collection.sortKeysDesc();

console.log(sorted.all());
```

**输出:**

```
{ section: 'A', score: 98, name: 'Rahul', dob: '25-10-96' }
```

**例 2:**

## java 描述语言

```
const collect = require("collect.js");

let obj = {
  sts_name: "Rakesh",
  id: "1005",
  course: "Web Technology",
  DOB: "15-12-91",
  section: "A",
};

const collection = collect(obj);

const sorted = collection.sortKeysDesc();

console.log(sorted.all());
```

**输出:**

```
{
  sts_name: 'Rakesh',
  section: 'A',
  id: '1005',
  course: 'Web Technology',
  DOB: '15-12-91'
}
```