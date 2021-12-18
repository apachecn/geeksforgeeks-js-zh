# 普通 JavaScript 中 GET 和 POST 请求的区别

> 原文:[https://www . geesforgeks . org/get-and-post-request-in-vanilla-JavaScript/](https://www.geeksforgeeks.org/difference-between-get-and-post-request-in-vanilla-javascript/)

在本文中，我们将学习普通 Javascript 中的 GET & POST 请求方法，还将通过示例了解这两种方法。

**GET** 和 **POST** 是两种不同类型的 **HTTP** 请求方法。 **HTTP** 协议支持多种方法从服务器传输数据或在服务器上执行任何操作。HTTP 协议支持 GET、POST、PUT、DELETE、PATCH、COPY、HEAD、OPTIONS 等方法。在深入探讨 **GET** 和 **POST** 请求方法的主要区别之前，我们先来看看这些 HTTP 方法是什么。

*   **GET 请求()方法:**正在从特定资源请求数据(通过某个应用编程接口网址)。在这个例子中，一个虚拟的应用编程接口被用来演示 GET 请求是如何工作的。
*   **POST 请求()方法:**数据被发送到特定的资源进行处理(通过一些 API URL)。在这个例子中，一个虚拟的应用编程接口被用来演示开机自检请求是如何工作的。

获取和发布请求方法由 [**获取()方法**](https://www.geeksforgeeks.org/javascript-fetch-method/) 使用，该方法用于向服务器请求并加载网页中的信息。

**示例:**该示例演示了 GET 请求方法。

## java 描述语言

```
// Instantiating new XMLHttpRequest() method
let xhr = new XMLHttpRequest();

// open() method to pass request
// type, url and async true/false 
xhr.open('GET',
    'https://jsonplaceholder.typicode.com/users/2', true);

// onload function to get data 
xhr.onload = function () {
    if (this.status === 200) {
        console.log(JSON.parse(this.responseText));
    }
}

// Send function to send data
xhr.send()
```

**示例:**该示例演示了 POST 请求方法。

## java 描述语言

```
// Instantiating new XMLHttpRequest()
let xhr = new XMLHttpRequest();

// open() method to pass request
// type, url and async true/false 
xhr.open('POST',
    'http://dummy.restapiexample.com/api/v1/create', true);

// Setting content-type
xhr.getResponseHeader('Content-type', 'application/json');

// Perform the following when the response is ready
xhr.onload = function () {
    if (this.status === 200) {
        console.log(this.responseText)
    }
    else {
        console.log("Some error occured")
    }
}

// Send the request as an object obj
obj = `{"name":"Selmon Bhoi", 
        "salary":"$10, 000", "age":"55"}`;
xhr.send(obj);
```

**GET 与 POST 的区别:**

<figure class="table">

| 

#### **s 号**T3】

 | 

#### **GET 请求**T3】

 | 

#### **开机自检请求**T3】

 |
| --- | --- | --- |
| 1。 | GET 检索指定资源的表示。 | POST 用于写入数据，待处理到已识别的资源。 |
| 2。

 | 它通常在请求的 URL 中有相关信息。 | 它通常在请求的正文中有相关信息。 |
| 3。 | 受浏览器和 web 服务器支持的 URL 最大长度限制。 | 它没有这样的限制。 |
| 4。 | 它是默认的 HTTP 方法。 | 在这种情况下，我们需要将方法指定为 POST 来用 POST 方法发送请求。 |
| 5。 | 可以为 GET 请求添加书签。

 | 您不能为开机自检请求添加书签。 |
| 6。 | 它不太安全，因为发送的数据是 URL 的一部分 | 它稍微安全一点，因为参数没有存储在浏览器历史记录或 web 服务器日志中。 |
| 7。 | 它是可缓存的。 | 不可缓存。 |
| 8。 | 获取显示特定问题的页面。 | 例如，通过点击“添加到购物车”按钮发送开机自检请求。 |

</figure>