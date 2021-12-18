# Fabric.js 文本框顶部属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-top-property/](https://www.geeksforgeeks.org/fabric-js-textbox-top-property/)

在本文中，我们将看到如何使用 top Property FabricJS 设置相对于画布顶部的位置。画布意味着文本框是可移动的，可以根据需要拉伸。此外，文本框可以在初始笔画颜色、填充颜色、笔画宽度或大小方面进行自定义。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并使用 top 属性设置相对于 Canvas 顶部的位置，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    top: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **顶部:**指定相对于顶部的位置。

**示例:**本示例使用 FabricJS 设置相对于画布文本框顶部的位置。

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
        Fabric.js | Textbox top Property
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
            top: 250
        });

        // Render the Textbox in canvas 
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/fcd83fc75bb437748727770d5c0c0c2d.png)