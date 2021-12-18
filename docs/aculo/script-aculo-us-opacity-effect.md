# 脚本. aculo.us 不透明度效果

> 原文:[https://www . geesforgeks . org/script-aculo-us-opacity-effect/](https://www.geeksforgeeks.org/script-aculo-us-opacity-effect/)

script.aculo.us **不透明度效果**是核心效果之一，它允许我们将元素的不透明度逐渐更改为给定的级别。此效果从元素的当前不透明度开始，除非定义了“从”选项，并以“到”选项定义的不透明度结束，默认不透明度值为 1.0。

**语法:**

```
new Effect.Opacity('id_of_element', [options]);

```

**示例 1:** 此示例显示如何将不透明度更改为显示或隐藏内容。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="./javascript/prototype.js">
    </script>

    <script type="text/javascript" 
src="./javascript/scriptaculous.js?load = effects">
    </script>

    <script type="text/javascript">
        function ShowElement(element) {
            new Effect.Opacity(element, { 
                duration: 1, from: 0, to: 1.0 });
        }

        function HideElement(element) {
            new Effect.Opacity(element, { 
                duration: 1, from: 1.0, to: 0 });
        }
    </script>
</head>

<body>
    <div onclick="ShowElement('element')">
        <Button>Show Content</Button>
    </div>
    <br />

    <div onclick="HideElement('element')">
        <Button>Hide Content</Button>
    </div>
    <br />
    <img id="element" src="./gfg.png">
</body>

</html>
```

**输出:**

![Out](img/38b83a234bd8f9f8fd036092292f5951.png)

**示例 2:** 更改内容的不透明度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="./javascript/prototype.js">
    </script>

    <script type="text/javascript" 
src="./javascript/scriptaculous.js?load = effects">
    </script>

    <script type="text/javascript">
        function ShowElement(element) {
            new Effect.Opacity(element, { 
                duration: 1.5, from: 0.5, to: 1.0 });
        }

        function HideElement(element) {
            new Effect.Opacity(element, { 
                duration: 1.5, from: 1.0, to: 0.3 });
        }
    </script>
</head>

<body>
    <div onclick="ShowElement('element')">
        <Button>Show Content</Button>
    </div>
    <br />

    <div onclick="HideElement('element')">
        <Button>Fade Content</Button>
    </div>
    <br />
    <img id="element" src="./gfg.png">
</body>

</html>
```

**输出:**

![Output](img/ac1cecb9cd129087ca1d76a616c8f2c1.png)