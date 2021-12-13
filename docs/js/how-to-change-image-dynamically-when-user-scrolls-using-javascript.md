# 当用户滚动时如何使用 JavaScript 动态改变图像？

> 原文:[https://www . geesforgeks . org/如何动态更改图像-当用户滚动时-使用-javascript/](https://www.geeksforgeeks.org/how-to-change-image-dynamically-when-user-scrolls-using-javascript/)

![](img/553446bddd207cc96172200adbb5c1bf.png)

我们将把这个功能添加到我们的网页中，这样每当用户在图像上向上或向下滚动时，图像就会改变。我们只使用了 3 个图像，但它可以很容易地扩展为多个图像。
我们将图像保持在彼此之上，这确保一次只能看到一个图像。当我们滚动时，我们减少当前图像的 z 坐标，增加新图像的 z 坐标。通过这样做，新图像覆盖旧图像，并且它出现在所有图像的顶部并且变得可见。

*   **HTML 代码:**用于创建包含图像的基本结构。

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <title>
        Change Image Dynamically
        when User Scrolls
    </title>
</head>

<body>
<h1>GeeksforGeeks</h1>
<b>A Computer Science Portal for Geeks</b>
    <div id="scroll-image">
        <img src="CSS.png" class="test" />
        <img src="html.png" class="test" />
        <img src="php.png" class="test" />
    </div>
</body>

</html>                   
```

*   **CSS 代码:** Css 用于设计结构。 [**位置属性**](https://www.geeksforgeeks.org/css-positioning-elements/) 是这里最重要的东西。它将使所有的图像出现在彼此之上。

## 超文本标记语言

```html
<style>
    body {
        text-align: center;
    }
    h1 {
        color: green;
    }
    img {
        position: absolute;
        left: 300px;
    }
</style>
```