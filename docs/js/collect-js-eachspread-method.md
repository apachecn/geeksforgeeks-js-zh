# Collect.js eachSpread()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-eachspread-method/](https://www.geeksforgeeks.org/collect-js-eachspread-method/)

**eachSpread()方法**用于迭代集合项，并将集合的每个嵌套项值传递给给定的回调函数。

**语法:**

```
collection.eachSpread()

```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 eachSpread()方法，如果您将其应用于对象集合，则该方法可以接受元素。

**返回值:**该方法迭代项目集合。

下面的例子说明了 collect.js 中的 eachSpread()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect([
    ['Rakesh', 80],
    ['Shyam', 94],
    ['Sandeep', 75],
    ['Ashok', 88]
]);

collection.eachSpread((name, marks) => {
    console.log("Name => " + name 
        + " | Marks => " + marks)
});
```

**输出:**

```
Name => Rakesh | Marks => 80
Name => Shyam | Marks => 94
Name => Sandeep | Marks => 75
Name => Ashok | Marks => 88

```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let arr = [
    ['Rahul', 98],
    ['Aditya', 96],
    ['Abhishek', 80],
];

// Converting object to collection 
const collection = collect(arr);

collection.eachSpread((name, score) => {
    console.log(name, score);
});

console.log(collection.eachSpread(
    (name, score) => false)
);
```

**输出:**

```
Rahul 98
Aditya 96
Abhishek 80
Collection {
 items: [ 
   [ 'Rahul', 98 ], 
   [ 'Aditya', 96 ], 
   [ 'Abhishek', 80 ] 
 ]
}

```