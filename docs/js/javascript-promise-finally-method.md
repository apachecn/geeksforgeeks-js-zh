# JavaScript Promise finally()方法

> 原文:[https://www . geesforgeks . org/JavaScript-promise-finally-method/](https://www.geeksforgeeks.org/javascript-promise-finally-method/)

Promise 对象的 **finally()方法**用于在承诺结算时返回一个承诺，即要么兑现要么拒绝。承诺是一个 JavaScript 对象，它在异步函数成功执行后生成一个值。当它由于超时而没有成功执行时，就会产生一个错误。

一旦承诺得到解决，它就可以用来执行清理任务，因为无论承诺是被履行还是被拒绝，它总是被执行。它还防止了 Promise 的 then()和 catch()方法中的代码重复。

**语法:**

```
task.finally(function() {
  // Task to be performed when
  // the promise is settled 
});
```

**参数:**该方法具有如上所述的单个参数，描述如下:

*   **最后:**是承诺结算时会调用的函数。

**返回值:**它返回一个 Promise，其最终处理程序被设置为指定的函数。

下面的示例演示了 finally()方法:

**例:**

## Javascript

```
// Define the Promise
let task = new Promise((resolve, reject) => {
  setTimeout(() => {

    // Reject the Promise
    reject("Promise has been rejected!");
  }, 2000);
});

task
  .then(
    (data) => {
      console.log(data);
    },

    // Handle any error
    (error) => {
      console.log("Error:", error);
    }
  )

  // Specify the code to be executed 
  // after the Promise is settled
  .finally(() => {
    console.log(
      "This is finally() block that is " +
      "executed after Promise is settled"
    );
  });
```

**输出:**

```
Error: Promise has been rejected!
This is finally() block that is executed after Promise is settled
```