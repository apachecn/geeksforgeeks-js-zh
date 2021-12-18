# Collect.js concat()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-concat-method/](https://www.geeksforgeeks.org/collect-js-concat-method/)

**concat()方法**用于返回集合所表示的合并数组或对象。JavaScript 数组首先被转换成一个集合，然后该函数被应用于该集合。

**语法:**

```
collect(array1).concat(array2)
```

**参数:**collect()方法接受一个转换为集合的参数，然后 concat()函数也接受一个数组。

**返回值:**返回合并的数组或对象。

下面的例子说明了 Collect.js 中的 **concat()方法**:

**示例 1:** 这里 collect = require(‘collect.js’)用于将 collect . js 库导入文件。

## Javascript

```
const collect = require('collect.js');  

let arr = [1, 2, 3]  

// Convert array into collection  
const collection = collect(arr);  

// concate the array
let concatarr = collection.concat(['a', 'b', 'c']);

// Returning the array 
let newObject =  concatarr.all();  

console.log("Result : ", newObject);
```

**输出:**

```
Result :  [ 1, 2, 3, 'a', 'b', 'c' ]
```

**例二:**

## Javascript

```
const collect = require('collect.js');  

let arr = [1, 2, 3]  

// Convert array into collection  
const collection = collect(arr);  

// concate the array
let concatarr = collection.concat(['a', 'b', 'c']);

// concate the object
concatarr = concatarr.concat({ first : "GeeksforGeeks", 
        second : "Collect.js"});

// Returning the array 
let newObject =  concatarr.all();  

console.log("Result : ", newObject);
```

**输出:**

```
Result :  [ 1, 2, 3, 'a', 'b', 'c', 'GeeksforGeeks', 'Collect.js' ]
```

**参考:**T2**https://collect.js.org/api/concat.html**T5】