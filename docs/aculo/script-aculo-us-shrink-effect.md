# 脚本 aculo.us 收缩效果

> 原文:[https://www . geesforgeks . org/script-aculo-us-shrink-effect/](https://www.geeksforgeeks.org/script-aculo-us-shrink-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示**收缩**的效果，将元素收缩到特定方向，并在效果完成时隐藏。我们也可以调整效果的持续时间。

**语法:**

```
Effect.Shrink('id_of_element');
```

//或

```
Effect.Shrink('id_of_element', { duration: dur });
```

//或

```
Effect.Shrink('id_of_element', { direction:'direction' });
```

**参数:**

*   **id_of_element:** 要应用效果的元素。
*   **持续时间:**该效果持续时间。
*   **方向:**要收缩的方向，默认为中心。

**注意:**要使用这个库，我们应该下载或安装这个库，然后在程序中使用它。要做到这一点，你可以跟随这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**进场:**

*   为了演示这个函数的用法，我们编写了一小段代码。其中我们写了一个小的 JavaScript 函数名为 **ShrinkEffect()** 方法，使用了这个库的 **Shrink()** 方法。
*   通过点击点击图像缩小，你会清楚地看到效果。

**示例 1:** 要查看效果，首先安装库，然后在本地环境中打开以下程序。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="prototype.js"></script>
    <script src=
        "scriptaculous.js?load = effects">
    </script>

    <script type="text/javascript">
        function ShrinkEffect(element) {
            new Effect.Shrink(element, { duration: 4 });
        }
    </script>
</head>

<body>
    <div id="myimage" onclick="ShrinkEffect(this);">
        <img height=200px width=200px 
            src="gfg.png" alt="gfg logo" />

        <h2>Click here to see the Shrink effect</h2>
    </div>
</body>

</html>
```

**输出:**

![](img/a9434559f39461f4b2b17f05962d1f91.png)

**示例 2:** 在这个示例中，我们使用了效果的方向作为“左下角”，并且还添加了一个按钮来显示效果。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="prototype.js"></script>
    <script src=
        "scriptaculous.js?load = effects">
    </script>

    <script type="text/javascript">
        function ShrinkEffect(element) {
            new Effect.Shrink(element, { duration: 1 });
        }
    </script>
</head>

<body>
    <div id="myimage" onclick="ShrinkEffect(this);">
        <img height=200px width=200px 
            src="gfg.png" alt="gfg logo" />
        <br><br>

        <button onclick="ShrinkEffect('myimage');">
            Click here to see the effect
        </button>
    </div>
</body>

</html>
```

**输出:**

![](img/f31b45ffadd1a9577fcdbf798866989c.png)