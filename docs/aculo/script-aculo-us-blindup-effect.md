# script.aculo.us BlindUp 效果

> 原文:[https://www . geeksforgeeks . org/script-aculo-us-blind up-effect/](https://www.geeksforgeeks.org/script-aculo-us-blindup-effect/)

在本文中，我们将通过使用一个名为 **script.aculo.us** 的 JavaScript 库来演示**隐藏**的效果。BlindUp 效果为元素提供了平滑的炫目过渡。我们也可以调整这个效果的持续时间。

**语法:**

```
Effect.BlindUp('id_of_element');
```

//或

```
Effect.BlindUp('id_of_element', [options]);
```

**选项:**

*   **持续时间:**持续时间取淡化元素，默认值为 1.0。
*   **scaleX:** 布尔值，默认为假。
*   **scaleY:** 布尔值，默认为真。
*   **scaleContent:** 布尔值，默认为真。
*   **scaleFromCenter:** 布尔值，默认为  false。
*   **缩放自:**整数值默认为 100。
*   **缩放模式:**用字符串值设置缩放模式，默认为‘框’。
*   **scaleTo:** 整数值默认为 100。

**注意:**要使用这个库，我们应该安装这个库，然后在我们的程序中使用它。而要做到这一点，你可以顺着这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**示例 1:** 为了演示这种效果的使用，我们编写了一小段代码。其中我们编写了一个名为 ShowEffect 方法的小 JavaScript 函数，使用了这个库的 **BlindUp** 方法。通过点击**点击我来屏蔽这条线！**，你会看清楚效果。

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
        function ShowEffect(element) {
            new Effect.BlindUp(element, 
            { duration: 1, from: 0, to: 1.0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowEffect('hideshow')">
        <button type="button">
            Click me to BlindUp the line!
        </button>
    </div>
    <br><br>

    <div id="hideshow">
        LINE TO BLIND UP
    </div>
</body>

</html>
```

**输出:**

![](img/ff99015cc0a6f1da59f6a8e772ea9472.png)

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
            new Effect.BlindUp(element, 
            { duration: 1, from: 0, to: 1.0 });
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

![](img/100ec12b02ea72cb580d1c8d8f68733e.png)