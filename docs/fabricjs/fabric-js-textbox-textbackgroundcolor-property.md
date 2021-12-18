# 织物. js 文本框文本背景颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-textbackgroundcolor-property/](https://www.geeksforgeeks.org/fabric-js-textbox-textbackgroundcolor-property/)

在本文中，我们将看到如何使用 FabricJS 的 textBackgroundColor 属性来更改画布 Textbox 的背景颜色。画布意味着所写的文本框是可移动的、可旋转的、可调整大小的，并且可以拉伸。但是在本文中，我们将更改背景颜色。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 textBackgroundColor 属性来更改背景颜色，并在 Textbox 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    textBackgroundColor: 'string'
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **textBackgroundColor:** 指定要设置的背景颜色。

**示例:**本示例使用 fabric js Textbox textBackgroundColor 属性设置画布文本框的背景颜色，如下所示:

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js | Textbox textBackgroundColor Property
    </h3>

    <canvas id="canvas" width="600" height="300" 
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Create a new Textbox instance 
        var text = new fabric.Textbox(
            'A Computer Science Portal', {
            width: 500,
            textBackgroundColor: "green"
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/2de0cea0099416018b60b8a4b73b3f58.png)