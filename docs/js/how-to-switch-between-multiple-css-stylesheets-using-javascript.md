# 如何使用 JavaScript 在多个 CSS 样式表之间切换？

> 原文:[https://www . geesforgeks . org/如何在多个 css 样式表之间切换-使用-javascript/](https://www.geeksforgeeks.org/how-to-switch-between-multiple-css-stylesheets-using-javascript/)

互联网上的许多网站都有多个主题。通过在 HTML 代码中制作多个样式表并一次启用一个样式表，可以获得任何特性。使用<link>标签将一个 CSS 文件包含到标签的 HTML 中。

```html
<link id="theme" rel="stylesheet" type="text/css" href="light.css" />

```

“href”属性指定了 CSS 文件的文件位置。通过改变这个标签，我们可以给网站添加新的 CSS。可以使用以下任何方法来实现。

**方法 1:** 当你想做一个开关或者切换按钮时，要切换 CSS。它根据当前活动的值在值之间切换。

## HTML

```html
<!DOCTYPE html>
<html>

<head>
    <!-- Add the style sheet. -->
    <link id="theme" rel="stylesheet" 
        type="text/css" href="light.css" />

    <script>
        function toggleTheme() {
            // Obtains an array of all <link>
            // elements.
            // Select your element using indexing.
            var theme = document.getElementsByTagName('link')[0];

            // Change the value of href attribute 
            // to change the css sheet.
            if (theme.getAttribute('href') == 'light.css') {
                theme.setAttribute('href', 'dark.css');
            } else {
                theme.setAttribute('href', 'light.css');
            }
        }
    </script>
</head>

<body>
    <h2>Changing Style Sheets</h2>
    <br />
    Click below button to switch between 
    light and dark themes.<br />

    <button onclick="toggleTheme()">Switch</button>
</body>

</html>
```