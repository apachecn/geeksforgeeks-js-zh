# Collect.js 管()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-pipe-method/](https://www.geeksforgeeks.org/collect-js-pipe-method/)

**pipe()方法**用于保存一个回调函数，并将该函数应用到集合中并返回相应的结果。

**语法:**

```
collect(array).pipe(callback)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 pipe()方法。pipe()方法将回调作为参数保存。

**返回值:**该方法返回应用于集合的回调函数的结果。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 pipe()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect([1, 
    2, 3, 5, 6, 8, 9, 11, 17, 22]);

// Function call
const pipe_val = collection.pipe(
    element => element.max());

// Printing the values
console.log(pipe_val);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
22
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect([1, 2,
    3, 5, 6, 8, 9, 11, 17, 22]);

// Function call
const pipe_sum = collection.pipe(
    element => element.sum());

// Printing the values
console.log(pipe_sum);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
84
```