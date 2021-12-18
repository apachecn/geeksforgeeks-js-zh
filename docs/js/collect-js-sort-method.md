# Collect.js 排序()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sort-method/](https://www.geeksforgeeks.org/collect-js-sort-method/)

**排序()方法**用于对集合的项目进行排序。

**语法:**

```
collect(array).sort()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sort()方法。

**返回值:**该方法排序后返回集合。

下面的例子说明了 collect.js 中的 sort()方法:

**例 1:**

```
const collect = require('collect.js'); 

let arr = [8, 4, 7, 6, 5, 11, 3]; 

const collection = collect(arr); 

const sorted = collection.sort();

let result = sorted.all();

console.log(result);
```

**输出:**

```
[3, 4, 5, 6, 7, 8, 11]
```

**例 2:**

```
const collect = require('collect.js'); 

let arr = [8, 4, 7, 6, 5, 11, 3]; 

const collection = collect(arr); 

const sorted = collection.sort((a, b) => b - a);

let result = sorted.all();

console.log(result);
```

**输出:**

```
[11, 8, 7, 6, 5, 4, 3]
```