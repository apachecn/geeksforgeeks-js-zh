# 如何在 JavaScript 中返回异步调用的响应？

> 原文:[https://www . geesforgeks . org/如何从异步 javascript 调用中返回响应/](https://www.geeksforgeeks.org/how-to-return-the-response-from-an-asynchronous-call-in-javascript/)

JavaScript 是一种单线程编程语言，异步编程是构建该语言的基础概念。有三种方法可以处理内置于 JavaScript 中的异步调用，如下所示:

*   回调函数
*   承诺和承诺处理。然后()和。catch()方法
*   使用 wait 的 ES6+/ESNext 风格异步函数

在本文中，我们将讨论如何以上述所有方式处理异步调用。我们将使用 Node.js 中提供的请求模块向网站 DOG CEO API 请求 JSON 数据，该 API 以 JSON 格式返回随机狗图片的 URL 链接。

1.  **Using a Callback function:**

    ```
    // Callback method
    const request = require('request');
    const url ='https://dog.ceo/api/breeds/image/random';

    function callback(res, body) { 
        console.log(JSON.parse(body));
    }

    function getData(callback) {

        // Using the request module to request
        // data asynchronously
        request(url, (err, res, body) => {
            if (err) throw err;
            callback(res, body);
        });
    }

    // Here we call the getData function
    // with the callback function 
    getData(callback);
    console.log('asynchronous is awesome');
    ```

    **输出:**

    ```
    asynchronous is awesome {
      message: 
    'https://images.dog.ceo/breeds/vizsla/n02100583_11450.jpg',  
      status: 'success'
    }

    ```

    **说明:**在这个方法中，我们为 JSON 数据请求 API，并使用回调函数对数据执行函数。为了便于理解，我们简单地将收到的数据记录到控制台上，但是可以执行各种其他功能。整个过程异步进行。命令`console.log('asynchronous is awesome');`虽然是在调用函数 getData 之后发出的，但在 getData 完成之前执行。

2.  **Using Promises with .then() and .catch() method:**

    ```
    // Promise with then catch
    const promise = new Promise((resolve, reject) => {
        request(url, (err, res, body) => {
            if (err) return reject(err);
            try {
                resolve(JSON.parse(body));
            } catch(error) {
                reject(error);
            }
        });
    });

    promise.then((data) => {
        console.log(data);
    })
    .catch((err)=>{
        console.error(err);
    });

    console.log('asynchronous is awesome');
    ```

    **输出:**

    ```
    asynchronous is awesome {
      message:
    'https://images.dog.ceo/breeds/pointer-germanlonghair/hans2.jpg',
      status: 'success'
    }

    ```

    **解释:**请求模块本身不返回承诺。因此，我们使用承诺构造函数将从 HTTP 请求接收到的可能响应包装成一个本机承诺。然后这个承诺被处理。然后()和。catch()方法。使用这种方法的优点是多方面的。首先，解决承诺。然后()和。catch()方法是错误处理的最佳实践，帮助我们以错误第一的心态编写代码。其次，JavaScript 模块正在适应支持承诺，并正在放弃旧的回调风格错误处理。像 Axios、fetch 等较新的模块只支持承诺。同样，Promises 是一种相对较新的编写异步代码的方式。事实证明了这一点，尽管命令`console.log('asynchronous is awesome');`是在调用承诺处理程序之后发出的，但它是在承诺完成之前执行的。

3.  **ES6+/ESNext style async functions using await:**

    ```
    const getData = async () => {
        let data = await new Promise((resolve, reject) => {
            request(url, (err, res, body) => {
                if (err) return reject(err);
                try{
                    resolve(JSON.parse(body));
                } catch(error) {
                    reject(error);
                }
            });
        });

        try{
            console.log(data);
        }
        catch(err){
            console.error(err);
        }
    }

    getData();
    console.log('asynchronous is best');
    ```

    **输出:**

    ```
    asynchronous is awesome {
      message: 
    'https://images.dog.ceo/breeds/sheepdog-shetland/n02105855_15196.jpg',
      status: 'success'
    }

    ```

    **解释:**Javascript 中的 Async 函数允许我们坚持传统的编程策略，例如使用 for、while 和其他方法，这些方法本质上是同步的，不能在 Javascript 中使用。在这个例子中，我们将 HTTP 请求返回的可能响应包装在一个承诺中。由于承诺需要一定的时间来解决或拒绝，我们使用 wait 关键字等待承诺返回响应。最佳实践是使用 try()/catch()序列来处理使用 await 后从 promise 收到的响应，以帮助我们处理错误(如果有)。虽然可以在 try()/catch()序列中写入同步代码，但异步函数是异步执行的，这一点可以通过以下事实来证明:命令`console.log('asynchronous is awesome');`虽然放在对函数 getData 的调用之后，但在异步函数完成之前执行。