# Collect.js sortBy()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-sortby-method/](https://www.geeksforgeeks.org/collect-js-sortby-method/)

**sortBy()方法**用于按照给定的关键字对集合进行排序。

**语法:**

```
collect.sortBy()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 sortBy()方法。

**返回值:**该方法按给定关键字排序后返回集合。

下面的例子说明了 collect.js 中的 sortBy()方法:

**例 1:**

```
const collect = require('collect.js'); 

let obj = [ 
    { 
        subject: 'English', 
        score: 95, 
    }, 
   { 
        subject: 'math', 
        score: 86, 
    },
    { 
        subject: 'science', 
        score: 90, 
    }
]; 

const collection = collect(obj); 

const sorted = collection.sortBy('score');

let result = sorted.all();

console.log(result);
```

**输出:**

```
 [
   { 
        subject: 'math', 
        score: 86, 
   }, 
   { 
        subject: 'science', 
        score: 90, 
   },
   { 
        subject: 'English', 
        score: 95, 
   }
]
```

**例 2:**

```
const collect = require('collect.js'); 

let obj = [ 
    { product_name: 'apple_laptop', price: 100000 },
    { product_name: 'apple_watch', price: 50000 },
    { product_name: 'apple_mobile', price: 80000 },
];

const collection = collect(obj); 

const sorted = collection.sortBy('price');

let result = sorted.all();

console.log(result);
```

**输出:**

```
[
    { product_name: 'apple_watch', price: 50000 },
    { product_name: 'apple_mobile', price: 80000 },
    { product_name: 'apple_laptop', price: 100000 }
]
```