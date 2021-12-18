# 如何检测 HTTP 或 HTTPS 然后在 JavaScript 中强制重定向到 HTTPS？

> 原文:[https://www . geesforgeks . org/how-to-detect-http-or-https-then-force-redirect-to-https-in-JavaScript/](https://www.geeksforgeeks.org/how-to-detect-http-or-https-then-force-redirect-to-https-in-javascript/)

**HTTPS** 代表**超文本传输协议安全**。顾名思义，它在用户的浏览器和他们试图访问的服务器之间创建了一个安全、加密的连接。由于这是一个加密连接，它可以防止恶意黑客窃取从用户浏览器传输到服务器的数据。在 HTTPS 有一个网站也告诉用户，他们可以信任你的网站。如果您在 HTTP 中有一个站点，并且在 HTTPS 有相同的版本，您可以自动将用户重定向到 HTTPS 站点。
为了实现这个重定向，我们将使用 JavaScript 代码。具体来说，我们将使用[**window . location . protocol**](https://www.geeksforgeeks.org/javascript-location-protocol-property/)属性来标识协议，然后使用 **window.location.href** 属性来重定向浏览器。**窗口位置**是**窗口**对象的属性。常用于 [**重定向**](https://www.geeksforgeeks.org/javascript-redirect-a-url/) 。**窗口.位置**返回一个**位置**对象，它包含许多有用的属性:

*   **协议:**这是浏览器窗口当前 URL 的协议(http:或 https:)。
*   **href:** 这是当前浏览器窗口的完整 URL。它是可写的。

**注意:**由于 **window.location.href** 是可写的，我们将为其设置一个新的 URL，从而用新的 URL 重新加载浏览器。

*   **例:**

## java 描述语言

```
if (window.location.protocol == 'http:') {

    console.log("you are accessing us via "
        +  "an insecure protocol (HTTP). "
        + "Redirecting you to HTTPS.");

    window.location.href =
        window.location.href.replace(
                   'http:', 'https:');
}
else
    (window.location.protocol == "https:") {
        console.log("you are accessing us via"
            + " our secure HTTPS protocol.");
    }
```

*   **输出:**

```
// On HTTP sites, you will be redirected to the HTTPS version.
```

**缺点:**从浏览器端设置 HTTPS 重定向有一些缺点。这些不利因素包括:

*   如果在你的连接中间有一个恶意黑客(中间人攻击)，他们可以阻止重定向的发生。
*   在 HTTP 的初始加载过程中，可能会有先前设置的 cookiess，现在黑客可以读取这些 cookie。

因此，我们建议在服务器端通过 HTTPS 重定向用户，而不是在 JavaScript 中。我们在下面添加了一个例子，说明如何使用用 Javascript 编写的服务器 [NodeJS](https://www.geeksforgeeks.org/introduction-to-nodejs/) 进行重定向。在服务器上使用 NodeJS，代码相似但不完全相同。我们将使用 **req.protocol** 来代替。

*   **示例(app.js):**

## java 描述语言

```
app.get('/', function(req, res, next) {
    if (req.protocol == 'http') {
        res.redirect('https://' +
        req.get('host') + req.originalUrl);
    }
});
```

*   **输出:**

```
// On HTTP sites, you will be redirected to the HTTPS version.
```

**注:****req . protocol**不包含冒号(如: **http** 或 **https** )，而 **window.location.protocol** 包含冒号(如: **http:** 和 **https:** )。