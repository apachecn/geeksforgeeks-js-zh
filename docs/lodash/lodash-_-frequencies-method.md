# 洛达什 _。频率()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-frequencies-method/](https://www.geeksforgeeks.org/lodash-_-frequencies-method/)

**洛达什 _。frequencies()方法**获取一个数组并返回一个映射对象，该对象的键是数组元素的值，而值是该数组中出现的键的计数。

**语法:**

```
_.frequencies( array );
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **数组:**要从中创建映射的给定数组。

**返回值:**这个方法返回一个创建的映射对象。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用以下命令安装 Lodash.js contrib 库:

```
npm install lodash-contrib
```

**例 1:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Array 
var array = ["Geeks", "Geeks", "GFG",  
             "Computer_Science_Portal",  
             "Geeks", "GFG"]; 

var obj = _.frequencies(array); 

// Printing object
console.log("Original Array : ", array); 
console.log("Frequency of elements : ", obj);
```

**输出:**

> 原始数组:[“极客”、“极客”、“GFG”、“计算机科学门户”、“极客”、“GFG”]
> 元素出现频率:对象{计算机科学门户:1，GFG: 2，极客:3}

**例 2:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Array 
var array = []; 

var obj = _.frequencies(array); 

// Printing object
console.log("Original Array : ", array); 
console.log("Frequency of elements : ", obj);
```

**输出:**

```
Original Array : []
Frequency of elements : Object {}
```

**例 3:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Array 
var array = [1, 1, 1, 1, 1, 1, 3,
          3, 3, 4, 4, 4, 5, 5, 5, 
          6, 6, 6, 6, 7, 7, 8, 10]; 

var obj = _.frequencies(array); 

// Printing array
console.log("Original Array : ", array); 
console.log("Frequency of elements : ", obj);
```

**输出:**

> 原始数组:[1，1，1，1，1，1，3，3，3，4，4，5，5，5，6，6，6，7，7，8，10]
> 元素频率:对象{1: 6，3: 3，4: 3，5: 3，6: 4，7: 2，8: 1，10: 1}