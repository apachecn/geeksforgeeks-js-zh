# JavaScript |承诺

> 原文:[https://www.geeksforgeeks.org/javascript-promises/](https://www.geeksforgeeks.org/javascript-promises/)

**承诺**用于处理 JavaScript 中的异步操作。当处理多个异步操作时，它们很容易管理，其中回调会创建回调地狱，导致无法管理的代码。

在承诺之前，使用了事件和回调函数，但是它们的功能有限，并且产生了难以管理的代码。
多个回调函数会创建回调地狱，导致无法管理的代码。此外，任何用户都不容易同时处理多个回调。
事件不擅长处理异步操作。

承诺是以最简单的方式处理异步操作的理想选择。它们可以轻松处理多个异步操作，并提供比回调和事件更好的错误处理。换句话说，我们可以说，承诺是同时处理多个回调的理想选择，从而避免了不希望的回调地狱情况。承诺确实为用户提供了一个更好的机会，以更有效的方式阅读代码，尤其是当特定代码用于实现多个异步操作时。

*   **承诺的好处**
    1.  提高代码可读性
    2.  更好地处理异步操作
    3.  异步逻辑中更好的控制定义流程
    4.  更好的错误处理
*   **承诺有四种状态:**
    1.  **履行**:与承诺相关的行动成功
    2.  **拒绝**:与承诺相关的行动失败
    3.  **待定**:承诺仍然待定，即尚未履行或拒绝
    4.  **已结算**:承诺已履行或已拒绝
*   **可以使用 promise 构造函数创建承诺。**
    **句法**

```
var promise = new Promise(function(resolve, reject){
     //do something
});
```

*   **参数**
    *   Promise 构造函数只接受一个参数，即回调函数(该回调函数也被称为匿名函数)。
    *   回调函数接受两个参数，*解析*和*拒绝*
    *   在回调函数中执行操作，如果一切顺利，就调用 resolve。
    *   如果所需操作不顺利，则呼叫拒绝。

**例**

## java 描述语言

```
var promise = new Promise(function(resolve, reject) {
  const x = "geeksforgeeks";
  const y = "geeksforgeeks"
  if(x === y) {
    resolve();
  } else {
    reject();
  }
});

promise.
    then(function () {
        console.log('Success, You are a GEEK');
    }).
    catch(function () {
        console.log('Some error has occurred');
    });
```

**输出:**

```
Success, You are a GEEK
```

**承诺消费者**
使用*注册功能即可消费承诺。然后是*和*。抓*方法。

**1。然后()**
*当承诺被解决或拒绝时，就会调用()*。它也可以被定义为从承诺中获取数据并进一步成功执行的职业。

**参数:**
*然后()*方法取两个函数作为参数。

1.  如果承诺得到解决并收到结果，则执行第一个功能。
2.  如果拒绝承诺并收到错误，则执行第二个功能。(可选，使用*有更好的处理错误的方法。赶()法*

**语法:**

```
.then(function(result){
        //handle success
    }, function(error){
        //handle error
    })
```

**示例:承诺已解决**

## java 描述语言

```
var promise = new Promise(function(resolve, reject) {
    resolve('Geeks For Geeks');
})

promise
    .then(function(successMessage) {
       //success handler function is invoked
        console.log(successMessage);
    }, function(errorMessage) {
        console.log(errorMessage);
    })
```

**输出:**

```
Geeks For Geeks
```

**示例:承诺被拒绝**

## java 描述语言

```
var promise = new Promise(function(resolve, reject) {
    reject('Promise Rejected')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    }, function(errorMessage) {
       //error handler function is invoked
        console.log(errorMessage);
    })
```

**输出:**

```
Promise Rejected
```

**2。catch()**

*当承诺被拒绝或执行中出现错误时，调用 catch()* 。只要在任何一步有可能出错，它就被用作错误处理程序。

**参数:**
*catch()* 方法以一个函数为参数。

1.  处理错误或拒绝承诺的功能。(.catch()方法在内部调用。然后(空，错误处理器)，即。catch()只是。然后(null，errorHandler))

**语法:**

```
.catch(function(error){
        //handle error
    })
```

**示例:承诺被拒绝**

## java 描述语言

```
var promise = new Promise(function(resolve, reject) {
    reject('Promise Rejected')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    })
    .catch(function(errorMessage) {
       //error handler function is invoked
        console.log(errorMessage);
    });
```

**输出:**

```
Promise Rejected
```

**示例:承诺被拒绝**

## java 描述语言

```
var promise = new Promise(function(resolve, reject) {
    throw new Error('Some error has occurred')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    })
    .catch(function(errorMessage) {
       //error handler function is invoked
        console.log(errorMessage);
    });
```

**输出:**

```
Error: Some error has occurred
```

**应用程序**

1.  承诺用于事件的异步处理。
2.  承诺用于处理异步 http 请求。

**参考**:[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。