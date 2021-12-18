# 【Fetch 和 Axios.js 发出 http 请求的区别

> 原文:[https://www . geesforgeks . org/fetch-and-axios-js-for-making-http-requests/](https://www.geeksforgeeks.org/difference-between-fetch-and-axios-js-for-making-http-requests/)

任何 web 应用程序的基本任务之一都是通过 HTTP 协议与服务器通信。这可以使用 Fetch 或 Axios 轻松实现。Fetch 和 Axios 在功能上非常相似。一些开发人员更喜欢 Axios，而不是内置的 API，因为它易于使用。提取应用编程接口完全能够再现 Axios 的关键功能。
[**Fetch:**](https://www.geeksforgeeks.org/fetch-api/)Fetch API 提供了在窗口对象上定义的 **fetch()方法**。它还提供了一个 JavaScript 接口，用于访问和操作 HTTP 管道的各个部分(请求和响应)。fetch 方法有一个强制参数-要获取的资源的 URL。此方法返回一个可用于检索请求响应的 Promise。

*   **节目:**

## java 描述语言

```
fetch('path-to-the-resource-to-be-fetched')
  .then((response) => {

    // Code for handling the response
  })
  .catch((error) => {

    // Code for handling the error
  });
```

**Axios:** Axios 是一个 Javascript 库，用来从 node.js 发出 HTTP 请求，或者从浏览器发出 XMLHttpRequests，它支持 JS ES6 自带的 Promise API。它可用于拦截 HTTP 请求和响应，并支持针对 XSRF 的客户端保护。它还能够取消请求。

*   **节目:**

## java 描述语言

```
axios.get('url')
  .then((response) => {

    // Code for handling the response
  })
  .catch((error) => {

    // Code for handling the error
  })
```

**Axios 与 Fetch 的区别:**

<figure class="table">取不到。

| 阿克斯 | 取得 |
| Axios has **URL** in the request object. | Fetch does not have [T0】 URL 【T1] in the request object. |
| Axios is a **independent third-party package** , which can be easily installed. | Fetch is built into most modern browsers; **No need to install** . |
| Axios enjoys built-in XSRF protection. |
| Axios uses the **data** attribute. | Fetch uses the **body** attribute. |
| Axios data contains the **object** . | Fetch's body must be **brushed** . |
| When **status is 200** **status is' ‘OK' 【T3], Axios request is normal. When the **response object contains the ok attribute** ,** | Get normal. |
| Axios performs **automatic conversion of JSON data** . | Fetch is a **two-step process** When processing JSON data-first, make an actual request; Second, call. Json () method on response. |
| Axios allows **cancellation of request and request timeout** . | I can't get it. |
| Axios has the ability **to intercept HTTP requests** . | Fetch does not provide a way to intercept requests by default. |
| Axios built-in support download progress. | Fetch does not support upload progress. |
| Axios has **wide browser support** . | Fetch only supports Chrome 42+, Firefox 39+, Edge 14+ and Safari 10.1+ (this is called backward compatibility). |

</figure>