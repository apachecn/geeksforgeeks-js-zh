# Fabric.js 文本框 skewX 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-skew x-property/](https://www.geeksforgeeks.org/fabric-js-textbox-skewx-property/)

在本文中，我们将看到如何使用 Fabric.js 设置画布 Textbox 的水平倾斜。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含 Textbox 的画布块。之后，我们将初始化 Fabric.js 提供的 Canvas 和 Textbox 的实例，使用 skewX 属性设置水平倾斜，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   skewX: number
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **偏斜:**指定水平偏斜角度，单位为度。

**示例:**本示例使用 Fabric.js 设置文本框的水平倾斜。

## 超文本标记语言

```
<html>
<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/4.3.0/fabric.min.js">
    </script>
</head>
<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>
    <h3>
        Fabric.js | Textbox skewX Property
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
            skewX: 200
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>
</html>
```

**输出:**

![](img/b021ce11bf303829afe0daf6cec919f9.png)