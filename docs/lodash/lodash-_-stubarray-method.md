# 洛达什 _。stubArray()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-stubarray-method/](https://www.geeksforgeeks.org/lodash-_-stubarray-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。stubArray()** 方法用于创建一个新的空数组。

**语法:**

```
_.stubArray()

```

**参数:**此方法不接受任何参数。

**返回值:**返回一个新的空数组。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubArray() method 
// to create an empty array
let arr = _.stubArray(); 

// Printing the output  
console.log(arr);
```

**输出:**

```
[]

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubArray() method
// to create 5 empty Array
let arr = _.times(5, _.stubArray); 

// Printing the output  
console.log(arr);
```

**输出:**

```
[[], [], [], [], []]

```