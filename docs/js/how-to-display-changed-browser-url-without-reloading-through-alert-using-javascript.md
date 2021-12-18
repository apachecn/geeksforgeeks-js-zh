# 如何使用 JavaScript 通过警报显示已更改的浏览器网址而不重新加载？

> 原文:[https://www . geesforgeks . org/如何显示-已更改-浏览器-URL-无需重新加载-通过-警报-使用-javascript/](https://www.geeksforgeeks.org/how-to-display-changed-browser-url-without-reloading-through-alert-using-javascript/)

要在不加载新页面的情况下更改浏览器中的网址，我们可以使用 JavaScript 中的 **[history.pushState()方法](https://www.geeksforgeeks.org/how-to-modify-url-without-reloading-the-page-using-javascript/)** 和 **[replaceState()方法](https://www.geeksforgeeks.org/how-to-modify-url-without-reloading-the-page-using-javascript/)** 。要在更改网址前显示浏览器网址，我们将在 alert()函数中使用 **window.location.href** ，并在更改浏览器网址后再次使用。

**注意:**History . pushState()方法结合了 HTML 5 History 和 JavaScript pushState()方法。

**语法:**

```
alert(" Message:" + window.location.hrf);
```

以下示例说明了上述方法:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript">
        function geeks() {
            alert("The current URL of this"
            + " page is: " + window.location.href);
        }

        function change_url() {
            window.history.pushState("stateObj",
                 "new page", "changedURL.html");

            alert("The URL of this page is: "
                    + window.location.href);
        }
    </script>
</head>

<body onload="geeks()">
    <a href="javascript:change_url()">
        Click to change url
    </a>
</body>

</html>
```

**输出:**
![](img/4fc2cc973ef08be7dbeff1d3ab308aaa.png)

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript">
        function geeks() {
            alert("The current URL of this "
            + "page is: " + window.location.href);
        }

        function change_url() {
            window.history.replaceState("stateObj",
                    "new page", "changedURL.html");

            alert("The URL of this page is: "
                    + window.location.href);
        }
    </script>
</head>

<body onload="geeks()">
    <a href="javascript:change_url()">
        Click to change url
    </a>
</body>

</html>
```

**输出:**
![](img/4fc2cc973ef08be7dbeff1d3ab308aaa.png)