# Collect.js 包含()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-contains-method/](https://www.geeksforgeeks.org/collect-js-contains-method/)

**contains()方法**用于确定集合是否包含给定的项目。如果它包含该项，则返回 true，否则返回 false。JavaScript 数组首先被转换成一个集合，然后该函数被应用于该集合。

**语法:**

```
collect(array).contains(item)
```

**参数:**该方法接受单个参数即转换成集合，然后包含()函数取一个待搜索项。

**返回值:**返回布尔值。

下面的例子说明了 Collect.js 中的**包含()方法**:

**示例 1:** 这里 collect = require(‘collect.js’)用于将 collect . js 库导入文件。

## Javascript

```
const collect = require('collect.js');  

let arr = [1, 2, 3];  

// Convert array into collection  
const collection = collect(arr);  

// item to searched
let item = 3;

let newObject = collection.contains(item);

console.log("Result : ", newObject);
```

**输出:**

```
Result :  true
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

// item to searched
let item = "GeeksforGeek";

let newObject = collection.contains(item);

console.log("Result : ", newObject);
```

**输出:**

```
Result : false
```

**参考:**T2】https://collect.js.org/api/contains.html