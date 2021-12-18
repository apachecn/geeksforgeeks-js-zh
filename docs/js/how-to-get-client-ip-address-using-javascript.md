# 如何使用 JavaScript 获取客户端 IP 地址？

> 原文:[https://www . geesforgeks . org/how-to-client-IP-address-use-JavaScript/](https://www.geeksforgeeks.org/how-to-get-client-ip-address-using-javascript/)

在本文中，我们将了解如何在 Javascript 中获取客户端的 IP 地址。一个 [IP 地址](https://www.geeksforgeeks.org/what-is-an-ip-address/)是一组数字的组合，唯一地标识一个人的系统。这就像一个房子，有一个接收邮件的地址。同样，您的计算机也有一个从网络接收数据的地址。[协议](https://www.geeksforgeeks.org/network-protocols/)一词指的是浏览全球连接时需要遵循的一些既定准则。[互联网](https://www.geeksforgeeks.org/what-is-internet-definition-uses-working-advantages-and-disadvantages/)的[网络](https://www.geeksforgeeks.org/what-is-computer-networking/)部分由互联网连接的确切规范(指南)定义。

为了获得客户端的公共 IP 地址，JavaScript 充当第三方服务器端语言。JavaScript 无法单独做到这一点，所以，添加了 jQuery 来做到这一点。JavaScript 与第三方应用程序一起工作来获取 IP 地址。这些应用服务获取用户的 IP 地址，并简单地以三种格式返回，即。、*纯文本*、 *JSON* 和 *JSONP* 格式。网上有很多。在这里，我们将使用[**【ipify】**](https://www.ipify.org)和 [**ipinfo**](https://ipinfo.io) ，这是两个最流行的寻找 IP 地址的工具。

**示例 1:** 在本例中，我们将使用包含 SSL 的网站(具有 https 协议)的 **ipify** 来获取客户端的 IP 地址。

## HTML

```
<!DOCTYPE html>
<html>

<head>
    <title>Getting Clients IP</title>
    <style>
    p, h1 {
        color: green;
    }
    </style>

    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js">
    </script>

      <script>

    /* Add "https://api.ipify.org?format=json" statement
               this will communicate with the ipify servers in
               order to retrieve the IP address $.getJSON will
               load JSON-encoded data from the server using a
               GET HTTP request */

    $.getJSON("https://api.ipify.org?format=json", function(data) {

        // Setting text of element P with id gfg
        $("#gfg").html(data.ip);
    })
    </script>
</head>

<body>
    <center>
        <h1>GeeksforGeeks</h1>
        <h3>Public IP Address of user is:</h3>
        <p id="gfg"></p>

    </center>
</body>

</html>
```