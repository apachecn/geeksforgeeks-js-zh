# Fabric.js 文本框编辑订单颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-editingordercolor-property/](https://www.geeksforgeeks.org/fabric-js-textbox-editingbordercolor-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布 textbox 的编辑文本框边框颜色。画布文本框意味着文本框是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   导入库后，我们将在主体标签中创建一个包含文本框的画布块。
*   之后，我们将初始化由 FabricJS 提供的 canvas 和 textbox 的实例，并使用 editingBorderColor 属性设置 canvas Textbox 的编辑边框颜色，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    editingBorderColor: string
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **editingordercolor:**指定编辑时的边框颜色。

**示例:**这里我们使用 FabricJS 设置画布文本框的编辑边框颜色。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox editingBorderColor Property
    </title>

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
        Fabric.js | Textbox editingBorderColor Property
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
            editingBorderColor: "green"
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/84fa9add4144fe7afbf68c1c2dcc07be.png)