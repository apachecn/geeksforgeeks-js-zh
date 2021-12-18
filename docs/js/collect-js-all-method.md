# Collect.js | all()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-all-method/](https://www.geeksforgeeks.org/collect-js-all-method/)

**all()方法**用于返回集合所表示的底层数组或对象。JavaScript 数组首先被转换成一个集合，然后该函数被应用于该集合。

**语法:**

```
collect(array).all()
```

**参数:**该方法不接受任何参数。

**返回值:**返回数组或对象。

下面的例子说明了 JavaScript 中的 **all()方法**:

**例 1:** 这里 collect = require('collect.js ')用于将 collect.js 库导入文件。

## java 描述语言

```
const collect = require('collect.js');

let arr = [1, 2, 3]

// Convert array into collection
const collection = collect(arr);

// Returning the array
let newObject =  collection.all();

console.log("Result : ", newObject);
```

**输出:**

```
Result : [1, 2, 3]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = { first : "GeeksforGeeks",
        second : "Collect.js"};

// Convert object into collection
const collection = collect(obj);

// Returning the object
let newObject =  collection.all();

console.log("Result : ", newObject);
```

**输出:**

```
Result :  { first: 'GeeksforGeeks', second: 'Collect.js' }
```

**参考:**T2https://collect.js.org/api/all.html