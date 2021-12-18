# script.aculo.us SlideUp 效果

> 原文:[https://www . geesforgeks . org/script-aculo-us-slide up-effect/](https://www.geeksforgeeks.org/script-aculo-us-slideup-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示 *SlideUp* 选项的视觉效果，该库具有从一个到另一个的平滑过渡。我们也可以调整效果的持续时间。

**语法:**

```
Effect.SlideUp('id_of_element');
```

或者

```
Effect.SlideUp('id_of_element', { duration: 3.0 });
```

**注意:**要使用这个库，我们应该下载这个库，然后在我们的程序中使用它。而要做到这一点你可以遵循这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**方法:**为了演示这个函数的使用，我们编写了一小段代码。我们已经编写了一个名为 *ShowEffect* 方法的小 JavaScript 函数，它使用了这个库的 *SlideUp* 方法。通过点击**点击我来滑动图像！**，你会看清楚效果的。

**示例:**要看效果，先安装库，然后在本地环境打开这个程序。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>

    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
        src="scriptaculous.js?load = effects">
    </script>

    <script type="text/javascript">

        function ShowEffect(element) {
            new Effect.SlideUp(element,
                { duration: 3.0 });
        }
        function displayImage(element) {
            new Effect.Appear(element, 
            { duration: 1, from: 1.1, to: 1.2 });
        }
    </script>
</head>

<body>
    <div onclick="displayImage('hideshow')">
        Click me to SlideUp the image!
    </div>
    <br />

    <div id="hideshow" onclick="ShowEffect(this);">
        <img src="GEEKSIMAGES/geeks1.PNG" alt="" /><br />
        Image to SlideUp
    </div>
</body>

</html>    
```

**输出:**

![](img/24d4139ecae832bcf9b4850d129e3874.png)