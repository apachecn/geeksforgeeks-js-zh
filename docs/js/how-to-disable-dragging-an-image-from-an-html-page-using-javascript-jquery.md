# 如何使用 JavaScript/jQuery 禁用从 HTML 页面拖动图像？

> 原文:[https://www . geesforgeks . org/如何使用 javascript-jquery/](https://www.geeksforgeeks.org/how-to-disable-dragging-an-image-from-an-html-page-using-javascript-jquery/) 禁用从 html 页面拖动图像

拖放是一个非常交互式和用户友好的概念，通过拖动可以更容易地将对象移动到不同的位置。它允许用户在一个元素上单击并按住鼠标按钮，将其拖动到另一个位置，然后释放鼠标按钮将该元素放在那里。在 HTML 5 中，拖放更容易编码，并且其中的任何元素都是可拖动的。默认情况下，链接和图像是可拖动的。大多数网站都启用了此功能。谷歌甚至允许用户使用图像拖放功能(也称为图像拖动功能)进行图像搜索。

该功能使用户能够点击任何图像，然后将其拖到其他地方。这将创建所单击图像的透明副本，同时保留原始图像。但是，可以使用 JavaScript/jQuery 禁用图像拖动功能。

**方法 1:** 该方法使用 jQuery 将 dtraggable 属性设置为 false。

**语法:**

```
$('#myImage').attr('draggable', false);
```

**示例:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to disable dragging an image
        from an HTML page using JQuery?
    </title>

    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js">
    </script>
</head>

<body style="text-align:center">
    <center>
    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        Click on the button to
        disable dragging an image
    </h3>

    <button onclick = "myGeeks()">
        Disable image dragging
    </button>

    <br>

    <img id="img" src=
"https://contribute.geeksforgeeks.org/wp-content/uploads/gfg-39.png">

    <script type="text/javascript">
        function myGeeks() {
            $('#img').attr('draggable', false);
        }
    </script>
</body>

</html>
```

**输出:**
![](img/f585abd74f1243bf677284683840f2fc.png)

**方法 2:** 该方法使用 JavaScript 将 dtraggable 属性设置为 false。

**语法:**

```
document.getElementById('myImage').draggable = false;
```

**示例:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to disable dragging an image
        from an HTML page using JQuery?
    </title>

    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js">
    </script>
</head>

<body style="text-align:center">
    <center>
    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        Click on the button to
        disable dragging an image
    </h3>

    <button onclick = "myGeeks()">
        Disable image dragging
    </button>

    <br>

    <img id="img" src=
"https://contribute.geeksforgeeks.org/wp-content/uploads/gfg-39.png">

    <script type="text/javascript">
        function myGeeks() {
            document.getElementById('img').draggable = false;
        }
    </script>
</body>

</html>
```

**输出:**
![](img/f585abd74f1243bf677284683840f2fc.png)