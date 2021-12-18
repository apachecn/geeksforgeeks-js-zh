# Javascript | mouse event ctrl key 属性

> 原文:[https://www . geesforgeks . org/JavaScript-mouse event-ctrl key-property/](https://www.geeksforgeeks.org/javascript-mouseevent-ctrlkey-property/)

**鼠标事件 ctrlKey** 属性用于定义是否按下 *ctrl* 键。它是一个布尔值。当按下 ctrl 键，然后点击鼠标按钮，它返回真，如果没有按下，它返回假。

**语法:**

```
event.ctrlKey
```

**返回值:**返回一个布尔值，表示是否按下 *ctrl* 键。

*   **真:**表示按了 ctrl 键。
*   **假:**表示没有按下 ctrl 键。

**示例:**

```
<!DOCTYPE html>
<html>
    <head>
        <title>JavaScript Mouse Event</title>
    </head>

    <body style = "text-align:center;">
        <h1 style = "color:green;">
            GeeksforGeeks
        </h1>

        <h2>
            mouseEvent ctrlKey Property
        </h2>

        <button onclick="geek (event);">Get Ctrl key state!</button>        
        <script>
        function geek (event) {
            if (event.ctrlKey) {
                alert ("Ctrl key is pressed.");
            }
            else {
                alert ("Ctrl key is not pressed.");
            }
        }
        </script>
    </body>
</html>
```

**输出:**
**点击按钮(ctrl 键未按下):**
![ctrlkey](img/8d14b7efb1664b455c8fc644193ace59.png)
**点击按钮(ctrl 键已按下):**
![ctrlkey](img/a96cc990e8c29ea53000605532a91892.png)

**支持的浏览器:**ctrl key 属性支持的浏览器如下:

*   苹果 Safari
*   谷歌 Chrome
*   火狐浏览器
*   歌剧
*   微软公司出品的 web 浏览器