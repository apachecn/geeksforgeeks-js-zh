# 脚本. aculo.us 出现效果

> 原文:[https://www . geesforgeks . org/script-aculo-us-appear-effect/](https://www.geeksforgeeks.org/script-aculo-us-appear-effect/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示**出现**的效果。外观效果为元素提供了平滑的外观过渡。我们也可以调整这个效果的持续时间。

**语法:**

```
Effect.Appear('element_id');
```

//或

```
Effect.Appear('element_id', [options]);
```

**选项:**

*   **持续时间:**淡入淡出元素的持续时间，默认值为 1.0。
*   **from:** 它是一个代表开始时不透明度百分比的浮点值，默认值为 0.0。
*   **到:**是表示不透明度百分比到结束的浮点值，默认值为 1.0。

**注意:**要使用这个库，我们应该安装这个库，然后在我们的程序中使用它。要做到这一点，你可以跟随这个链接[http://script.aculo.us/downloads](http://script.aculo.us/downloads)。

**示例 1:** 为了演示这个函数的用法，我们编写了一小段代码。其中我们编写了一个名为 ShowEffect 方法的小 JavaScript 函数，它使用了这个库的出现方法。通过点击**点击我出现的线路！**，你会看清楚效果。

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
            new Effect.Appear(element, 
            { duration: 1, from: 0, to: 1.0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowEffect('geeks_1')">
        <button type="button">
            Click me to Appear the line!
        </button>
    </div>
    <br />
    <br />

    <div id="geeks_1">
        LINE TO APPEAR
    </div>
</body>

</html>
```

**输出:**

![](img/35520ec9ef72b0767c323ac0f487e89c.png)

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
            new Effect.Appear(element, 
            { duration: 1, from: 0, to: 1.0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowEffect('geeks_1')">
        <button type="button">
            Click me to Appear the line!
        </button>
    </div>
    <br />
    <br />

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

![](img/0dc25b0f28c664842a741bd7a4d3e82c.png)