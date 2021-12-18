# Collect.js tap()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-tap-function/](https://www.geeksforgeeks.org/collect-js-tap-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。点击 **()** 功能接受收藏作为参数，在不影响收藏的情况下，它允许用户在特定点点击**进入收藏，并对物品进行任何操作。**

****安装:**使用以下命令安装 **Collect.js** 模块:**

```
npm install --save collect.js
```

****语法:****

```
collection.tap(callback)
```

****参数:**该函数只取一个参数，即根据用户需要执行的回调函数。**

****返回值:**该函数返回新的集合对象。**

****示例 1:Filename-index . js****

## **Javascript**

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [2, 4, 3, 1, 5]

// Function call
var newCollection = collect(myCollection)
.tap((collection) => {
    // Printing collection
    console.log(collection.all());
})

console.log(newCollection)
```

**使用以下命令运行 **index.js** 文件:**

```
node index.js
```

****输出:****

```
[ 2, 4, 3, 1, 5 ]
Collection { items: [ 2, 4, 3, 1, 5 ] }
```

****示例 2:Filename-index . js****

## **Javascript**

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [-1,2,0,25]

// Sorting and displaying result
collect(myCollection).sort().tap((collection) => {
    console.log(collection.all());
})
```

**使用以下命令运行 **index.js** 文件:**

```
node index.js
```

****输出:****

```
[ -1, 0, 2, 25 ]
```

****参考:**T2】https://collect.js.org/api/tap.html**