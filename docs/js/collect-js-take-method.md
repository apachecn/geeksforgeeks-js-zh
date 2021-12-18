# Collect.js take()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-take-method/](https://www.geeksforgeeks.org/collect-js-take-method/)

**take()方法**用于返回具有指定项目数的新集合。如果作为参数传递的参数为负，它将返回集合末尾的元素。

**语法:**

```
collect.take()
```

**参数:**collect()方法获取一个转换为集合的参数，然后对其应用 take()方法。

**返回值:**这个方法返回一个具有指定项数的新集合。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 take()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js'); 

// Sample array
let arr = [2, 4, 5, 6, 7, 8, 9]; 

// Creating collection
const collection = collect(arr); 

// Function call
const result = collection.take(5)

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
[2, 4, 5, 6, 7]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js'); 

// Sample array
let arr = ['a', 'b', 'c', -3, 4, -6, 7]; 

// Creating collection
const collection = collect(arr); 

// Function call
const result = collection.take(-3)

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
[4, -6,  7]
```