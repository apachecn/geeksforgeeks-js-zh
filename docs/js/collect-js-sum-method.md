# Collect.js sum()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sum-method/](https://www.geeksforgeeks.org/collect-js-sum-method/)

collect.js 中的 **sum()方法**用于返回给定集合中所有项目的总和。

**语法:**

```
collect(array).sum()
```

**参数:**collect()方法获取一个参数，该参数被转换为集合，然后 sum()方法被应用于该参数。

**返回值:**此方法返回集合中所有项目的总和:

下面的例子说明了 collect.js 中的 sum()方法:

**例 1:**

## java 描述语言

```
// Acquiring collect.js constant
const collect = require('collect.js'); 

let arr = [5, 10, 12, 15, 18] 

const collection = collect(arr);

const find_sum = collection.sum(); 

console.log(find_sum);
```

**输出:**

```
60
```

**例 2:**

## java 描述语言

```
// Acquiring collect.js constant
const collect = require('collect.js'); 

let obj = [ 
    { 
        subject: 'English', 
        score: 85, 
    }, 
   { 
        subject: 'math', 
        score: 90, 
    },
    { 
        subject: 'science', 
        score: 98, 
    }
]; 

const collection = collect(obj); 

const find_sum = collection.sum('score'); 

console.log(find_sum);
```

**输出:**

```
273
```