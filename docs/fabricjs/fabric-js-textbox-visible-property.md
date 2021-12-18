# Fabric.js 文本框可见属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-visible-property/](https://www.geeksforgeeks.org/fabric-js-textbox-visible-property/)

在本文中，我们将看到如何使用 FabricJS 中的**可见属性**来设置画布文本框的可见性。画布意味着文本框是可移动的，可以根据需要拉伸。此外，文本框可以在初始笔画颜色、填充颜色、笔画宽度或大小方面进行自定义。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并使用 visible 属性设置 canvas Textbox 的可见性，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    visible: boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **可见:**指定对象的可见性。

**示例:**本示例使用 FabricJS Textbox visible Property 将画布文本框的可见性设置为 false，因此文本将不可见。

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
        Fabric.js | Textbox visible Property
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
            visible: false
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/f4b12d0b512914b0dc97321879fffceb.png)