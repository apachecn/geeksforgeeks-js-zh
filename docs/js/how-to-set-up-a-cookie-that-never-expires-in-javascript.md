# 如何在 JavaScript 中设置永不过期的 cookie？

> 原文:[https://www . geesforgeks . org/如何设置永不过期的 JavaScript cookie/](https://www.geeksforgeeks.org/how-to-set-up-a-cookie-that-never-expires-in-javascript/)

我们可以使用以下方法在 JavaScript 中设置一个永不过期的 cookie:

**先决条件:**

*   JavaScript 中级知识
*   基本 HTML strong

**免责声明:**所有饼干按照[饼干规格](http://www.faqs.org/rfcs/rfc2965.html)过期。因此，没有任何代码块可以用 JavaScript 编写来设置永不过期的 cookie。这是不可能的，也是事实。

**解决方案:**但是您可以设置一个在 JavaScript 中过期的 cookie，并选择一些非常大的值作为过期日期，如下所示:

```html
document.cookie = "cookieName= true; expires=Fri, 31 Dec 9999 23:59:59 GMT";
```

**注意:**但是浏览器对 **2038-01-19 04:14:07** 之后的日期有问题，因为 Unix 纪元时间超过 32 位 int。这个问题也叫[**2038 年问题**](https://en.wikipedia.org/wiki/Year_2038_problem) (也叫 Y2038、划时代、Y2k38、或 Unix Y2K)。

因此，您可以为大多数 web 浏览器支持的 cookie 设置的最大过期日期是:

```html
2<sup>31</sup> - 1 = 2147483647 ie. 2038-01-19 04:14:07
```

**语法:**

```html
document.cookie = "cookieName= true; expires=Tue, 19 Jan 2038 04:14:07 GMT";

// OR
const cookieName = "something";
const cookieValue = "something";
const daysToExpire = new Date(2147483647 * 1000).toUTCString();
document.cookie = cookieName + '=' + cookieValue + '; expires=' + daysToExpire;
```

**代码:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script type="text/javascript">
        const createCookieWithY2K38 = (cookieName, cookieValue) => {

            // Expiry date conversion into UTC standard string
            const daysToExpire = new Date(2147483647 * 1000).toUTCString();

            // Setting up the cookie name, value with the expiry date
            document.cookie =
                cookieName + '=' + cookieValue + '; expires=' + daysToExpire;
            alert('Welcome ' + cookieValue);
        }
        const extractUserNameFromCookie = (cookieName) => {
            var userName = cookieName + '=';

            // Splitting cookie
            var allCookieArray = document.cookie.split(';');
            for (var i = 0; i < allCookieArray.length; i++) {

                // Extracting userName and returning the same
                var temp = allCookieArray[i].trim();
                if (temp.indexOf(userName) == 0)
                    return temp.substring(userName.length, temp.length);
            }

            // Else return empty string
            return '';
        }
        const readCookieAndGreetUser = () => {
            var userName = extractUserNameFromCookie('testCookie');
            if (userName != '') {
                //  If user is visiting the page again
                // "user" variable will not be a empty string
                // returned by the accessCookie() function
                // and will greet the user
                alert('Welcome ' + userName);
            }
            else {
                userName = prompt('Please enter your name');
                if (userName != '' && userName != null) {
                    createCookieWithY2K38('testCookie', userName);
                }
            }
        }
    </script>
</head>
<body onload="readCookieAndGreetUser()"></body>
</html>
```

**输出:**

![](img/22db7fd59f21eca4aa8f2a1ff6585349.png)

持久的饼干