# 脚本 aculo.us 折叠效果

> 原文:[https://www.geeksforgeeks.org/script-aculo-us-fold-effect/](https://www.geeksforgeeks.org/script-aculo-us-fold-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示**折叠**的效果，该库首先在垂直方向上平滑缩小，然后向左水平缩小，最后消失。我们也可以调整效果的持续时间。

**语法:**

```
Effect.Fold('id_of_element');

// Or

Effect.Fold('id_of_element', { duration: dur });
```

**参数:**

*   **id_of_element:** 要应用效果的元素。
*   **持续时间:**该效果持续时间。

**注意:**要使用这个库，我们应该下载或安装这个库，然后在我们的程序中使用它。要做到这一点，你可以跟随这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**进场:**

*   为了演示这个函数的用法，我们编写了一小段代码。其中我们编写了一个名为 **FoldEffect()** 方法的小 JavaScript 函数，使用了这个库的 **Fold()** 方法。
*   点击点击这里查看折叠效果，你会清楚地看到效果。

**示例 1:** 要查看效果，首先安装库，然后在本地环境中打开以下程序。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src = "prototype.js"></script>

    <script src = 
        "scriptaculous.js?load = effects">
    </script>

    <script type = "text/javascript">
        function FoldEffect(element){
            new Effect.Fold(element, {duration:4});
        }
    </script>
</head>

<body>
    <div id = "myimage" onclick = "FoldEffect(this);">

        <img height=200px width=200px 
            src = "gfg.png" alt = "gfg logo" />

        <h2>Click here to see the Fold effect </h2>
    </div>    
</body>

</html>
```

**输出:**

![](img/6b48e3751b13e654333ebb015de9c2ca.png)

**示例 2:** 在这个示例中，我们更改了效果的持续时间，还添加了一个按钮来查看效果。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src = "prototype.js"></script>

    <script src = 
        "scriptaculous.js?load = effects">
    </script>

    <script type = "text/javascript">
        function FoldEffect(element){
        new Effect.Fold(element, {duration:3});
        }
    </script>
</head>

<body>
    <div id = "myimage">
        <img height=200px width=200px 
            src = "gfg.png" alt = "gfg logo" />

        <br><br>

        <button onclick = "FoldEffect('myimage');">
            Click here to see the effect
        </button>
    </div>    
</body>

</html>
```

**输出:**

![](img/e0b7f3a1954a1686adbea7e3bd56d943.png)