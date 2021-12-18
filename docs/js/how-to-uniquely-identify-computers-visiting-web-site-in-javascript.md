# 如何在 JavaScript 中唯一识别访问网站的计算机？

> 原文:[https://www . geesforgeks . org/如何唯一识别计算机-访问-javascript 网站/](https://www.geeksforgeeks.org/how-to-uniquely-identify-computers-visiting-web-site-in-javascript/)

如果你想识别访问你的网站的计算机，你必须将你的网站的 cookies 存储在访问的计算机上。

**Cookies:** 简单来说，HTTP cookies 就是存储用户对某个特定网站偏好的小笔记。例如，当用户在没有登录的情况下在线购物时，他可能会将一些物品放入购物车。即使在关闭浏览器并重新加载网站后，存储在购物车中的项目也不会发生任何变化。用户的这些数据作为 cookie 存储在用户的计算机中。因此，下次用户访问网站时，数据可以返回到网站服务器。因此，网站能够唯一地识别计算机。

关于 **[的更多细节，cookies 在网站中是如何使用的？](https://www.geeksforgeeks.org/cookies-used-website/)T3】**

**饼干工序:**

*   每当计算机访问您的网站时，服务器都会向浏览器发送一个键值格式的 cookie。一旦浏览器接受了 cookie，它就会作为文本记录存储在计算机硬件中。
*   现在，当计算机访问您的网站时，该 cookie 会从计算机中检索并发送到服务器。这样，服务器识别访问网站的计算机，并记住以前的数据交换。

**JavaScript 中的 Cookies:**JavaScript 可以使用 **[document.cookie](https://www.geeksforgeeks.org/html-dom-cookie-property/)** 属性进行读取、创建和删除 Cookies 等所有操作。cookie 文本记录由四个属性组成。

1.  **Name-value or key-value:** These are the only attribute pairs sent from the browser to the server when the computer repeatedly visits the website. All Rest attributes are only used by browsers to determine other attributes.
2.  **Domain and path:** The domain name of the website that controls the authority of the website on the Internet. Set the directory of cookie or the path of web pages.
3.  **Secure and HTTP ONLY:** Secure is used to keep cookie exchange limited to encrypted transmission and instruct browsers to use cookies only through secure/encrypted connections. **HTTP ONLY** instructs the browser not to disclose cookies through channels other than **HTTP** (and HTTPS) requests.
4.  **expires and max-age:** expires defines the time that cookie are stored in the browser, after which they will be deleted. If blank, the cookie will expire when the visitor exits the browser.

**示例:**以下示例演示了 cookies，它存储 cookies 2 天，并使用 cookies 用用户的语言向用户打招呼。运行此代码后，系统会要求您输入语言“英语/西班牙语”。输入后，您可以再次运行代码，并看到系统用选定的语言向用户问好。

```
<!DOCTYPE html>
<html>
    <head>
    <script>
        function setCookie(cookieName, cookieValue) {
            var d = new Date();
            d.setTime(d.getTime() + 2 * 24 * 60 * 60 * 1000);
            var expires = "expires=" + d.toGMTString();
            document.cookie = cookieName + "=" 
            + cookieValue + ";" + expires + ";path=/";
        }
        function getCookie(cookieName) {
            var name = cookieName + "=";
            var decodedCookie = decodeURIComponent(document.cookie);
            var cookieArray = decodedCookie.split(";");
            for (var i = 0; i < cookieArray.length; i++) {
                var cookie = cookieArray[i];
                while (cookie.charAt(0) == " ") {
                    cookie = cookie.substring(1);
                }
                if (cookie.indexOf(name) == 0) {
                    return cookie.substring(name.length, cookie.length);
                }
            }
            return "";
        }
        function checkCookie() {
            var language = getCookie("language");
            if (language != "") {
                if (language == "english") alert("Hello Friend!");
                else if (language == "spanish") alert("Hola Amigo!");
            }
            language = prompt
            ("Please enter language[english/spanish]:", "");
            if (language != "" && language != null) {
                if (language == "english") 
                document.write
                ("You selected english! Now RUN it again.");
                else if (language == "spanish") 
                document.write
                ("You selected spanish! Now RUN it again.");
                setCookie("language", language);
            }
        }
    </script>
    </head>
    <body onload="checkCookie()"></body>
</html>                    
```

**输出:**如果选择“英语”，则给出提醒消息框，然后是文档消息。

```
  Hello Friend!
  You selected english! Now RUN it again.

```

cookie 不能保证用户下次访问网站时能够识别计算机。发生这种情况有三个原因。

*   Users have full rights to delete cookies and clear cache.
*   Cookie are built to identify browsers. Next time, if users visit your website through different browsers, cookies will be stored in two browsers respectively.
*   If the user turns off local cookie support in the browser, cookies will not work.

要始终识别访问您网站的计算机，您必须在访问的计算机上编写系统应用程序。