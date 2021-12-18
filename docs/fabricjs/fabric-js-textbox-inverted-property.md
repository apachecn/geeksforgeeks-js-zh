# Fabric.js 文本框反转属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-inverted-property/](https://www.geeksforgeeks.org/fabric-js-textbox-inverted-property/)

在本文中，我们将看到如何使用 Fabric.js 设置 Textbox 画布的反转属性。Fabric.js 中的文本框可以根据需要进行拉伸。此外，文本框可以自定义初始笔画颜色、填充颜色、笔画宽度或半径。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含 Textbox 的画布块。之后，我们将初始化由 Fabric.js 提供的 Canvas 和 Textbox 的实例，并使用反转属性设置 Textbox 的反转属性，并在 Canvas 上呈现它，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    inverted: boolean
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **反转:**它是一个布尔值，用于设置文本框的反转属性。

**示例:**本示例使用 Fabric.js 设置画布 Textbox 的反转属性。

## 超文本标记语言

```
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
        Fabric.js | Textbox inverted Property
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
            inverted: false
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>
</html>
```

**输出:**

![](img/b462bba43f1486aee26e2389cd672b23.png)