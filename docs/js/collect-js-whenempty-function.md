# Collect.js whenEmpty()功能

> 原文:[https://www . geesforgeks . org/collect-js-when empty-function/](https://www.geeksforgeeks.org/collect-js-whenempty-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。**when empty()**功能在集合为空时执行回调功能。

**安装:**使用以下命令安装 **Collect.js** 模块:

```
npm install --save collect.js
```

**语法:**

```
collection.whenEmpty(callback)
```

**参数:**该函数只取一个参数，即当集合为空时执行的回调函数。

**返回值:**该函数返回新的集合对象。

**示例 1:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = []

// Creating collection object
const collection = collect(myCollection);

// Callback exection since collection object is empty
collection.whenEmpty(item => item.push('Greetings'));

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Greetings' ]
```

**示例 2:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = ['One', 'Two', 'Three']

// Creating collection object
const collection = collect(myCollection);

// No callback execution since collection is not empty
collection.whenEmpty((item) => {
  item.push('Four')
  item.push('Five')
  item.push('Six')
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
[ 'One', 'Two', 'Three']
```

**参考:**T2】https://collect.js.org/api/whenEmpty.html