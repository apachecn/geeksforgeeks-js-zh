# collect . js unassembly()函数

> 原文:[https://www . geeksforgeeks . org/collect-js-unlesassembty-function/](https://www.geeksforgeeks.org/collect-js-unlessempty-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。**取消集合()**功能在集合不为空时执行回调功能。

**安装:**使用以下命令安装 **Collect.js** 模块:

```
npm install --save collect.js
```

**语法:**

```
collection.unlessEmpty(callback)
```

**参数:**该函数只取一个参数，即如果集合不为空时执行的回调函数。

**返回值:**该函数返回新的集合对象。

**示例 1:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [1, 2]

// Creating collection object
const collection = collect(myCollection);

// Callback execution since collection
// object is not empty
collection.unlessEmpty(item => item.push(3));

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 1, 2, 3 ]
```

**示例 2:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = []

// Creating collection object
const collection = collect(myCollection);

// No callback execution since
// collection is not empty
collection.unlessEmpty((item) => {
  item.push(1)
  item.push(2)
});

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ ]
```

**参考:**T2】https://collect.js.org/api/unlessEmpty.html