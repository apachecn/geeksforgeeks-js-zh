# 如何用 Javascript 画布创建逼真的雨滴效果？

> 原文:[https://www . geesforgeks . org/how-create-reality-雨滴-effect-with-JavaScript-canvas/](https://www.geeksforgeeks.org/how-to-create-realistic-raindrops-effect-with-javascript-canvas/)

在本文中，我们将学习如何使用 JavaScript [画布](https://www.geeksforgeeks.org/html-canvas-basics/)创建逼真的雨滴效果。

我们在我们的网站中使用这种雨滴效果来使它们更加美丽，从而增加用户交互。假设有一个网站，我们有一张季风的图片，但是如果图片是静态的，没有显示雨滴，那么我们可以把这个应用到它上面，使它变得真实。

为了实现上述功能，我们使用了一个名为 *rainyday.js* 的开源库，使用 canvas 元素来包含这样的效果。

**方法:**我们使用一个名为 [rainyday.js](https://github.com/mubaidr/rainyday.js) 的预构建库。转到下载文件夹，提取 *rainyday.js* 的 zip 文件，然后导航到目录“src”。复制 *rainyday.js* 文件并粘贴到项目文件夹中。

![](img/2f2b03efac972da277630c7fc3c16835.png)

文件夹结构

打开 *src* 文件夹，可以看到项目中使用的 *rainyday.js* 库文件。

![](img/6be29cd99af5b2cb328a822fb539d741.png)

打开 src 文件夹以获取所需的库文件

**示例:**创建一个*index.html*文件，并在文件的头部链接 *rainyday.js* 文件以使用库。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">

    <title>Rain Effect</title>

    <style>
        /* Adding css to the body */

        body {
            height: 100%;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }
        /* setting Image height*/

        img {
            height: 100%;
        }
    </style>
</head>

<body onload="render();">
    <img src="" alt="" id="back">

    <script>

        // Creating a function when our document loads 
        function render() {

            var image = document.getElementById('back');
            image.onload = function() {

                // Initiating a object of rainyday library
                var engine = new RainyDay({
                    image: this
                });

                // Now rendering them on the screen 
                // first element - size of drops,
                // second element - size of effect drops produced
                // third element - Quantity of drops
                engine.rain([
                    [10, 5, 10]
                ], 100);
            };
            image.src =
'https://media.geeksforgeeks.org/wp-content/uploads/20210802132841/geeks.jpg';
        }
    </script>

    <!-- Linking rainyday.js library file -->
    <script src="src/rainyday.js"></script>
</body>

</html>
```

**输出:**

![](img/d1970b603f2719f99d188d8c862fafb8.png)

雨天效应