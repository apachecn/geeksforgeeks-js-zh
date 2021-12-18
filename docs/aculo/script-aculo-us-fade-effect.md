# 脚本. aculo.us 淡入淡出效果

> 原文:[https://www.geeksforgeeks.org/script-aculo-us-fade-effect/](https://www.geeksforgeeks.org/script-aculo-us-fade-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示**淡化**的效果。淡入淡出效果为元素提供了平滑的淡入淡出过渡。我们也可以调整这个效果的持续时间。

**语法:**

```
Effect.Fade('element_id');
```

//或

```
Effect.Fade('element_id', options );
```

**选项:**

*   **持续时间:**淡化元素所用的持续时间，默认为 1.0。
*   **from:** 它是一个代表开始时不透明度百分比的浮点值，默认值为 0.0。
*   **到:**是表示不透明度百分比到结束的浮点值，默认值为 1.0。

**注意:**要使用这个库，我们应该安装这个库，然后在我们的程序中使用它。而要做到这一点，你可以顺着这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**示例 1:** 为了演示这个函数的用法，我们编写了一小段代码。其中我们编写了一个名为 ShowEffect 方法的小 JavaScript 函数，它使用了这个库的 **Fade** 方法。点击**点击我淡化线条！**，你会看清楚效果。

若要查看效果，请先安装库，然后在本地环境中打开此程序。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
        src="scriptaculous.js?load = effects,controls">
    </script>

    <script type="text/javascript">
        function ShowAction(element) {
            new Effect.Fade(element, 
            { duration: 1, from: 0, to: 1.0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowAction('hideshow')">
        <button type="button">
            Click me to Fade the line!
        </button>
    </div>
    <br><br>

    <div id="hideshow">
        LINE TO FADE
    </div>
</body>

</html>
```

**输出:**

![](img/cecfdc4c4bed22053a9bfe4b0d734d66.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
    src="scriptaculous.js?load = effects,controls">
    </script>

    <script type="text/javascript">
        function ShowEffect(element) {
            new Effect.Fade(element, 
            { duration: 2, from: 0, to: 1.0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowEffect('geeks_1')">
        <button type="button">
            Click me to ShowEffect!
        </button>
    </div>
    <br><br>

    <div id="geeks_1">
        <div style="width: 10%; height: 10%; 
            background-color: green;">
            Geeks For Geeks
        </div>
    </div>
</body>

</html>
```

**输出:**

![](img/d772d0828021408fd45ae322d8dffb19.png)