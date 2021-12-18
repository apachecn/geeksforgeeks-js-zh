# Collect.js 拼接()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-splice-method/](https://www.geeksforgeeks.org/collect-js-splice-method/)

**拼接()方法**用于移除并返回从指定索引开始的项目切片

**语法:**

```
collect(array).splice()
```

**参数:**collect()方法获取一个参数，该参数被转换为集合，然后对其应用 splice()方法。

**返回值:**这个方法返回一个从指定索引开始的项目切片。

下面的例子说明了 collect.js 中的 splice()方法:

**例 1:**

```
const collect = require('collect.js'); 

let arr = [8, 4, 7, 6, 5, 11, 3]; 

const collection = collect(arr); 

const spliced = collection.splice(3);

let result1 = spliced.all();
let result2 = collection.all();

console.log(result1);
console.log(result2);
```

**输出:**

```
[6, 5, 11, 3]
[8, 4, 7]
```

**例 2:**

```
const collect = require('collect.js'); 

let arr = [8, 4, 7, 6, 5, 11, 3]; 

const collection = collect(arr); 

const spliced = collection.splice(4, 5);

let result1 = spliced.all();
let result2 = collection.all();

console.log(result1);
console.log(result2);
```

**输出:**

```
[5, 11, 3]
[8, 4, 7, 6]
```