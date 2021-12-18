# Collect.js takeWhile()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-takewhile-method/](https://www.geeksforgeeks.org/collect-js-takewhile-method/)

**takeWhile()方法**用于返回集合中的项目，直到给定的回调返回 false。如果回调从未返回 false，takeWhile()方法将返回集合中的所有项。

**语法:**

```
collect.takewhile()
```

**参数:**collect()方法获取一个转换为集合的参数，然后对其应用 takeWhile()方法。

**返回值:**该方法返回集合中的项目。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的例子说明了 collect.js 中的 takeWhile()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js'); 

// Sample array
let arr = [1, 2, 3, 4, 5, 6, 8, 9]; 

// Creating collection
const collection = collect(arr); 

// Function call
const result = collection
    .takeWhile(item => item < 8);

// Printing the result object
let newObject = result.all();
console.log(newObject);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[1, 2, 3, 4, 5, 6]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js'); 

// Sample array
let arr = [2, 4, 5, 6, 7, 8, 9]; 

// Creating collection
const collection = collect(arr); 

// Function call
const result = collection
    .takeWhile(item => item != 11);

// Printing the result object
let newObject = result.all();
console.log(newObject);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[2, 4, 5, 6, 7, 8, 9]
```