# 为什么我们在 JavaScript 中使用 then()方法？

> 原文:[https://www . geesforgeks . org/why-we-use-then-method-in-JavaScript/](https://www.geeksforgeeks.org/why-we-use-then-method-in-javascript/)

JavaScript 中的 **then()** 方法已经在 Promise API 中定义，用于处理异步任务，比如 API 调用。以前，回调函数被用来代替这个函数，这使得代码难以维护。

**语法:**

```html
demo().then(
    (onResolved) => {
        // Some task on success
    },
    (onRejected) => {
        // Some task on failure
    }
)

Note: demo is a function that returns a promise prototype.
```

**参数:**该功能有两个参数来处理承诺的成功或拒绝:

*   **完成:**这是一个在承诺成功时调用的函数。这是一个可选参数。
*   **弹出:**这是一个在拒绝承诺时调用的函数。这是一个可选参数。

**返回值:**该方法可以返回一个承诺(如果再调用另一个承诺，则()或者不返回任何承诺。

**示例 1:不传递参数**

## Java Script 语言

```html
<script type="text/javascript">
    function demo() {
      document.write("Function called!!<br>")
      return Promise.resolve("Success");
      // or
      // return Promise.reject("Failure");
    }
    demo().then()
 </script>
```

**输出:**

```html
Function called!!
```

**例 2:只传递第一个回调**

## Java Script 语言

```html
<script type="text/javascript">
    function demo() {
      document.write("Function called!!<br>")
      return Promise.resolve("Success");
      // or
      // return Promise.reject("Failure");
    }
    demo().then(
      (message) => {
        document.write("Then success:" + message);
      }
    )
</script>
```

**输出:**

```html
Function called!!
Then success:Success
```

请注意，如果演示功能返回拒绝，那么它将产生一个错误。

**示例 3:** **通过两个参数**

## Java Script 语言

```html
<script type="text/javascript">
    function demo() {
      document.write("Function called!!<br>")
      return Promise.resolve("Success");
      // or
      // return Promise.reject("Failure");

    }
    demo().then(
      (message) => {
        document.write("Then success:" + message);
      },
      (message) => {
        document.write("Then failure:" + message);
      }
    )
</script>
```

**输出:**

```html
Function called!!
Then success:Success
```

**示例 4:** **链接多个 then()方法:**每个 then()可以返回一个承诺(一个解决或一个拒绝)，因此多个 then()方法可以链接在一起。

## Java Script 语言

```html
<script type="text/javascript">
    function demo() {
      document.write("Function called!!<br>")
      return Promise.resolve(1);
      // or
      // return Promise.reject("Failure");

    }
    demo().then(
      (value) => {
        document.write(value);
        return ++value;
      },
      (message) => {
        document.write(message);
      }
    ).then(
      (value) => {
        document.write(value);
      },
      (message) => {
        document.write(message);
      }
    )
</script>
```

**输出:**

```html
Function called!!
12 
```

**示例 5:** **使用 then()作为异步函数**

## Java Script 语言

```html
<script type="text/javascript">
    var demo = new Promise((resolve, reject) => {
      resolve(1);
    })
    let call = demo.then(
      (value) => {
        console.log(value);
        return ++value;
      },
      (message) => {
        document.write(message);
      });
    console.log(call);
    setTimeout(() => {
      console.log(call);
    });
</script>
```

**控制台输出:**

```html
Promise {status: "pending"}
1
Promise {status: "resolved", result: 2}
```

**支持的浏览器:**

*   谷歌 Chrome 6.0 及以上版本
*   Internet Explorer 9.0 及以上版本
*   Mozilla 4.0 及以上版本
*   Opera 11.1 及以上
*   Safari 5.0 及以上版本