# Collect.js 唯一()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-unique-method/](https://www.geeksforgeeks.org/collect-js-unique-method/)

**unique()方法**用于返回集合中的所有唯一值。

**语法:**

```
collect(array).unique()
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 unique()方法。

**返回值:**该方法返回集合中所有唯一的项目。

下面的例子说明了 collect.js 中的 unique()方法:

**例 1:**

```
const collect = require('collect.js'); 

let arr = [1, 2, 3, 4, 5, 4, 3, 2, 1]; 

const collection = collect(arr); 

const unique = collection.unique();

let newObject =  unique.all();   

console.log(newObject);
```

**输出:**

```
[1, 2, 3, 4, 5]
```

**例 2:**

```
const collect = require('collect.js'); 

let obj = [ 
    { 
        name: 'Kripamoy', 
        dob: '03-03-98', 
        section: 'A', 
        score: 94, 
    }, 
    { 
        name: 'Biltu', 
        dob: '23-01-96', 
        section: 'B', 
        score: 85, 
    }, 
    { 
        name: 'Santanu', 
        dob: '23-01-98', 
        section: 'B', 
        score: 98, 
    },
    { 
        name: 'chinmoy', 
        dob: '18-08-97', 
        section: 'A', 
        score: 72 
    } 
]; 

const collection = collect(obj); 

const unique = collection.unique('section');

let newObject =  unique.all();   

console.log(newObject);
```

**输出:**

```
[
 {name: "Kripamoy", dob: "03-03-98", score: 94, section: "A"},
 {name: "Biltu", dob: "23-01-96", score: 85, section: "B"}
]
```