# 如何用 JavaScript 检测网站是在移动设备上打开还是在桌面上打开？

> 原文:[https://www . geesforgeks . org/如何检测网站是在移动设备中打开还是在 javascript 桌面中打开/](https://www.geeksforgeeks.org/how-to-detect-whether-the-website-is-being-opened-in-a-mobile-device-or-a-desktop-in-javascript/)

使用[CSS Media query](https://www.geeksforgeeks.org/css-media-queries/)，我们可以很容易地知道用户当前正在哪个设备中查看我们的网站([使用最小宽度和最大宽度](https://www.geeksforgeeks.org/how-to-target-desktop-tablet-and-mobile-using-media-query/))。它只限于设计网页的样式，但是我们可以使用 JavaScript 中的*导航用户代理*属性根据用户的设备来控制网站的功能。

我们可以获得关于用户设备的信息。它返回一个包含用户浏览器名称、版本、操作系统等的字符串。

**语法:**

```
navigator.userAgent 
```

**返回类型:**它为 Windows 桌面返回以下字符串*:*

```
*Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) 
Chrome/90.0.4430.85 Safari/537.36*
```

***示例:**使用该属性，我们可以很容易地预测它是在桌面或移动设备上打开的，如下代码所示。*

 *## HTML

```
<html>
<body>
    <script>
        /* Storing user's device details in a variable*/
        let details = navigator.userAgent;

        /* Creating a regular expression 
        containing some mobile devices keywords 
        to search it in details string*/
        let regexp = /android|iphone|kindle|ipad/i;

        /* Using test() method to search regexp in details
        it returns boolean value*/
        let isMobileDevice = regexp.test(details);

        if (isMobileDevice) {
            document.write("You are using a Mobile Device");
        } else {
            document.write("You are using Desktop");
        }
    </script>
</body>
</html>
```* 

***输出:**以下是桌面浏览器的输出:*

```
*You are using Desktop*
```