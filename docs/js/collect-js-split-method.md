# Collect.js 拆分()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-split-method/](https://www.geeksforgeeks.org/collect-js-split-method/)

collect.js 中的 **split()方法**用于将一个集合分解成给定数量的组。

**语法:**

```
collect(array).split()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 split()方法。

**返回值:**该方法返回一个通过拆分主集合而得到的集合。

下面的例子说明了 collect.js 中的 split()方法:

**例 1:**

## Javascript

```
// Acquiring collect.js constant
const collect = require('collect.js'); 

let arr = [1, 2, 3, 4, 5, 6, 7]; 

const collection = collect(arr);

const groups = collection.split(4); 

let newObject = groups.all();

console.log(newObject);
```

**输出:**

```
[[1, 2], [3, 4], [5, 6], [7]]
```

**例二:**

## Javascript

```
// Acquiring collect.js constant
const collect = require('collect.js'); 

let arr = [['c', 'c++'], ['java'], ['python', 'c#']] 

const collection = collect(arr);

const groups = collection.split(3); 

let newObject = groups.all();

console.log(newObject);
```

**输出:**

```
[[['c', 'c++']], [['java']], [['python', 'c#']]]
```