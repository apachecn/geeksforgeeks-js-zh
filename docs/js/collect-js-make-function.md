# Collect.js make()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-make-function/](https://www.geeksforgeeks.org/collect-js-make-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。**使** **()** 功能创建一个新的收藏实例。

**安装:**使用以下命令安装 **Collect.js** 模块:

```
npm install --save collect.js
```

**语法:**

```
collection.make(user collection)
```

**参数:**该函数只取一个参数，即用户集合，即用户定义的集合。

**返回值:**该函数返回新的集合对象。

**示例 1:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [1,2,3,4,5]

function make(items = []) {
    return new this.constructor(items);
}

// Creating collection object
const collection = collect(myCollection);

// Printing collection
console.log(collection.all());

// Make Function call
console.log(make([1,2,3]))
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 1, 2, 3, 4, 5 ]
[ 1, 2, 3 ]
```

**示例 2:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = ['Monday', 'Tuseday', 'Thursday',
    'Friday', 'Saturday', 'Sunday']

// Function definition
function make(items = []) {
    return new this.constructor(items);
}

// Creating collection object
const collection = collect(myCollection);

// Make Function call
console.log(make(collection))
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Collection {
  items: [ 'Monday', 'Tuseday', 'Thursday', 
    'Friday', 'Saturday', 'Sunday' ]
}
```

**参考:**T2】https://collect.js.org/api/make.html