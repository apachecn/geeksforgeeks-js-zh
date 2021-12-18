# collect . js unlesnotempty()函数

> 原文:[https://www . geesforgeks . org/collect-js-unless notempty-function/](https://www.geeksforgeeks.org/collect-js-unlessnotempty-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。当集合为空时，**unlesnotempty()**函数执行回调函数。

**安装:**使用以下命令安装 **Collect.js** 模块:

```
npm install --save collect.js
```

**语法:**

```
collection.unlessNotEmpty(callback)
```

**参数:**该函数只取一个参数，即当集合为空时执行的回调函数。

**返回值:**该函数返回新的集合对象。

**示例 1: Filename-index.js**

## java 描述语言

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = []

// Creating collection object
const collection = collect(myCollection);

// Callback execution since collection object is empty
collection.unlessNotEmpty(item => item.push(1));

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 1 ]
```

**示例 2: Filename-index.js**

## java 描述语言

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [1, 2, 3]

// Creating collection object
const collection = collect(myCollection);

// No callback execution since
// collection is not empty
collection.unlessNotEmpty((item) => {
  item.push(4)
  item.push(5)
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
[ 1, 2, 3]
```

**参考:**T2】https://collect.js.org/api/unlessNotEmpty.html