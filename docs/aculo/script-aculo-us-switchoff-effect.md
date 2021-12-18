# 脚本 aculo.us 关闭效果

> 原文:[https://www . geesforgeks . org/script-aculo-us-switch off-effect/](https://www.geeksforgeeks.org/script-aculo-us-switchoff-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示 *SwitchOff* 选项的视觉效果，该库具有从一个到另一个的平滑过渡。我们也可以调整效果的持续时间。

**语法:**

```
Effect.SwitchOff('id_of_element');
```

**注意:**要使用这个库，我们应该下载这个库，然后在我们的程序中使用它。而要做到这一点你可以遵循这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**演示:**为了演示这个功能的使用，我们写了一小段代码。我们已经编写了一个小的 JavaScript 函数 *ShowEffect()* 方法，它使用了这个库的 *SwitchOff()* 方法。通过点击**点击我来关闭线路！**，你会看清楚效果的。

**示例:**要查看效果，首先在代码中包含库文件，然后在本地环境中打开这个程序。

## 超文本标记语言

```
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
            new Effect.SwitchOff(element, 
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
        Click me to display the image!
    </div>
    <br />

    <div id="hideshow" onclick="ShowEffect(this);">
        <img src="GEEKSIMAGES/geeks1.PNG" alt="" /><br />
        Click me to switch me off.
    </div>
</body>

</html>
```

**输出:**

![](img/4e4686126b5657f92167645626a9b1eb.png)