# 普通 JavaScript 中 PUT 和 DELETE 请求的区别

> 原文:[https://www . geeksforgeeks . org/put-and-delete-request-in-vanilla-JavaScript/](https://www.geeksforgeeks.org/difference-between-put-and-delete-request-in-vanilla-javascript/)

**PUT** 和 **DELETE** 是两种不同类型的 **HTTP** 请求方法。 **HTTP** 协议支持多种方法从服务器传输数据或者在服务器上做任何操作。 **HTTP** 协议支持以下方法，如 GET、POST、PUT、DELETE、PATCH、COPY、HEAD、OPTIONS 等。在深入探讨 PUT 和 DELETE 请求方法之间的主要区别之前，让我们先来看看 **HTTP** 方法。

**什么是 PUT 请求方法？**
当客户端在请求 URL 下发送替换文档或向 Web 服务器上传新文档时使用。

**什么是 DELETE 请求方法？**
当客户端试图从网络服务器删除文档时使用，由请求网址标识。

**示例:**让我们来看一个 PUT 请求方法的示例。

## java 描述语言

```
function easyHTTP() {

    // Initialising new XMLHttpRequest method.
    this.http = new XMLHttpRequest();
}

// Make an HTTP PUT Request
easyHTTP.prototype.put = function (url, data, callback) {

    // Open an object (POST, PATH,
    // ASYNC-TRUE/FALSE)
    this.http.open('PUT', url, true);

    // Set content-type
    this.http.setRequestHeader(
        'Content-type', 'application/json');

    // Assigning this to self to have scope
    // of this into the function onload()
    let self = this;

    // When the response is ready
    this.http.onload = function () {

        // Callback function (Error, response text)
        callback(null, self.http.responseText);
    }

    // Since the data is an object so
    // we need to stringify it
    this.http.send(JSON.stringify(data));
}

// Instantiating easyHTTP
const http = new easyHTTP;

// Data that we need to update
const data = {
    title: ‘Custom Putt’,
    body: ‘This is a custom put’
};

// Put prototype method(url,data,response text)
http.put(
    'https://jsonplaceholder.typicode.com/posts/5',
    data, function (err, post) {

        if (err) {
            console.log(err);
        }
        else {
            console.log(post);
        }

    });
```

**示例:**下面的代码演示了 DELETE 请求方法。

## java 描述语言

```
function easyHTTP() {

    // Initialising new XMLHttpRequest method.
    this.http = new XMLHttpRequest();
}

// Make an HTTP Delete Request
easyHTTP.prototype.delete = function (url, callback) {

    // Open an object (GET/POST, PATH,
    // ASYNC-TRUE/FALSE)
    this.http.open('DELETE', url, true);

    // Assigning this to self to have 
    // scope of this into the function
    let self = this;

    // When the response is ready
    this.http.onload = function () {

        // Checking status
        if (self.http.status === 200) {

            // Callback function(Error, response text)
            callback(null, 'Post Deleted');
        } else {

            // Callback function (Error message)
            callback('Error: ' + self.http.status);
        }
    }

    // Send the request
    this.http.send();
}

// Instantiating easyHTTP
const http = new easyHTTP;

// Delete prototype method(URL,
// callback(error,response text))
http.delete(
    'https://jsonplaceholder.typicode.com/posts/1',
    function (err, response) {
        if (err) {
            console.log(err);
        } else {
            console.log(response);
        }
    });
```

**PUT 和 DELETE 的区别:**

<figure class="table">

| **put request** | **删除请求** |
| Used to create or modify resources. | Used to delete the resources identified by the URL. |
| It is idempotent. | It is also idempotent. |
| When the resource is successfully created, the HTTP success code is 201 (created). | After successfully deleting the record, we can see 200 (normal) or 204 (no content). |

</figure>