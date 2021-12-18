# Fabric.js 文本框角度属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-angle-property/](https://www.geeksforgeeks.org/fabric-js-textbox-angle-property/)

在本文中，我们将看到如何使用 Fabric.js 设置画布 Textbox 中对象的旋转角度。Fabric.js 中的 Textbox 是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

**方法:**为了使其成为可能，我们将使用一个名为 Fabric.js 的 JavaScript 库，在使用 CDN 导入库之后，我们将在 body 标签中创建一个画布块，其中将包含我们的 Textbox。之后，我们将初始化画布和文本框的实例，使用 angle 属性将文本旋转到所需的角度，并在文本框上呈现画布，如下例所示。

**语法:**

```
new fabric.Textbox('text', {
    angle: number
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **角度:**指定旋转角度。

**示例:**本示例使用 Fabric.js 创建一个 Textbox 并使其可旋转。

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
        Fabric.js | Textbox angle Property
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
            width: 450,
            angle: 30
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>
</html>
```

**输出:**

![](img/ce70c28a113a73321fcf9a2fca1b38b7.png)