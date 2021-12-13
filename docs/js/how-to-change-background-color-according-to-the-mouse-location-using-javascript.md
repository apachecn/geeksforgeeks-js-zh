# 如何使用 JavaScript 根据鼠标位置改变背景颜色？

> 原文:[https://www . geesforgeks . org/如何更改背景色-根据鼠标位置-使用 javascript/](https://www.geeksforgeeks.org/how-to-change-background-color-according-to-the-mouse-location-using-javascript/)

使用 DOM(文档对象模型)可以根据光标位置改变背景颜色。在本文中，我们使用光标的位置来设置背景的值。

**方法:**方法是利用 DOM 操作，根据特定时间的光标位置改变背景。

**HTML 代码:**在本节中，我们有一个简单的带有 div 标签的 HTML 锅炉板代码。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content=
        "width=device-width, 
        initial-scale=1.0" />

    <title>
        How to change background 
        color according to mouse 
        location using JavaScript?
    </title>
</head>

<body>
    <div class="geeks"></div>
</body>

</html>
```

**CSS 代码:**在 CSS 中，我们刚刚设置了背景色为封面。

```html
<style>
    .geeks {
        width: 100%;
        height: 600px;
        background-size: cover;
    }
</style>
```

**注意:**可以设置默认背景。

**Javascript 代码:**在 JS 中，首先使用 querySelector 函数选择 div 标签，我们有 offset 属性来获取光标在二维平面即 X 轴和 Y 轴上的位置。现在我们使用坐标设置背景值。

```html
<script>
    var div = 
        document.querySelector(".geeks");

    div.addEventListener(
        "mousemove", function (e) {
        x = e.offsetX;
        y = e.offsetY;
        div.style.backgroundColor 
            = `rgb(${x}, ${y}, ${x - y})`;
    });
</script>
```

**完整代码:**是以上三段代码的组合。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
    <title>
        How to change background color
        according to mouse location
        using JavaScript ?
    </title>

    <style>
        .geeks {
            width: 100%;
            height: 600px;
            background-size: cover;
        }
    </style>
</head>

<body>
    <div class="geeks"></div>

    <script>
        var div =
            document.querySelector(".geeks");

        div.addEventListener(
            "mousemove", function (e) {
                x = e.offsetX;
                y = e.offsetY;
                div.style.backgroundColor
                    = `rgb(${x}, ${y}, ${x - y})`;
            });
    </script>
</body>

</html>
```

**输出:**
![](img/f6c5282c2f5ad551568d3e608c7c399f.png)