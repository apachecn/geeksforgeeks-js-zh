# 如何用 JavaScript 清除所有 cookies？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 清除所有 cookie/](https://www.geeksforgeeks.org/how-to-clear-all-cookies-using-javascript/)

**[Cookies](https://www.geeksforgeeks.org/http-cookies/)** 为客户端和服务器提供了一种通过 HTTP 进行交互和传递信息的方式。这使得客户端能够存储状态信息，尽管使用的是无状态协议 HTTP。当浏览器向服务器请求网页时，服务器服务于该请求并“忘记”访问。但是它会将一些信息传递给用户的浏览器。浏览器以键值对的形式存储信息，并管理这些信息。

*   在用户浏览器对域的每次后续访问中，Cookie 信息都会在 HTTP 请求头中传递。
*   登录细节、同意、其他偏好等信息用于增强和定制用户体验。

HTTP cookies 过期，日期和时间在“过期”属性中指定。因此，当日期和时间超过过期日期(和时间)时，浏览器会自动删除 cookies。由于该属性是可配置的*，因此可以通过将“到期时间”设置为任何已经过去的值来删除所有 cookies。

当前文档的 cookie 属性用于修改使用 **[HTML DOM cookie 属性](https://www.geeksforgeeks.org/html-dom-cookie-property/)** 购买的 cookie 的属性。 **document.cookie** 返回与当前文档相关的所有 cookies 的单个字符串，用分号分隔。

**语法:**

```
document.cookie = "key=value";
```

**代码:**下面的代码说明了如何使用 JavaScript 删除 cookies。该代码在一个在线编辑器上运行，以演示只有您的站点创建的 cookies 才能被该代码删除。

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>
        Clear cookies using Javascript
    </title>
</head>

<body>
    <center>
        <h1 style="color:green">
             GeeksforGeeks
        </h1>
        <script type="text/javascript">
            document.cookie = "1P_JAR=akjdsbJKHdjhbk";
            document.cookie = "CONSENT=YES+IN.en+20170903-09-0";

            function displayCookies() {

                var displayCookies = document.getElementById("display");
                displayCookies.innerHTML = document.cookie;
            }

            function deleteCookies() {
                var allCookies = document.cookie.split(';');

                // The "expire" attribute of every cookie is 
                // Set to "Thu, 01 Jan 1970 00:00:00 GMT"
                for (var i = 0; i < allCookies.length; i++)
                    document.cookie = allCookies[i] + "=;expires="
                    + new Date(0).toUTCString();

                displayCookies.innerHTML = document.cookie;

            }
        </script>
        <button onclick="displayCookies()">Display Cookies</button>
        <button onclick="deleteCookies()">Delete Cookies</button>
        <p id="display"></p>
    </center>
</body>

</html>

```

**输出:**
![](img/7a4e67fa2ca0209df646de5038770867.png)
**注意:**如果 cookie 的属性“HTTP”设置为“True”，则无法使用 JavaScript 修改其任何属性。