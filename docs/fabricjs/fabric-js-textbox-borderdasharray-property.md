# fabric . js Textbox bordersharray 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-textbox-bordersharray-property/](https://www.geeksforgeeks.org/fabric-js-textbox-borderdasharray-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布文本框边框的虚线图案。画布意味着文本框是可移动的，可以根据需要拉伸。此外，文本框可以自定义初始笔画颜色、填充颜色、笔画宽度或半径。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。
*   在此之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并使用 borderDashArray 属性设置 canvas Textbox 边框的虚线模式，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    borderDashArray: array
});
```

**参数:**该功能接受如上所述的单个参数，如下所述:

*   **边框线:**此参数定义边框的虚线图案。

**示例:**本示例使用 FabricJS 设置画布状文本框的边框虚线图案，如下所示。请注意，您必须单击椭圆才能看到边框。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox borderDashArray Property
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
        Fabric.js | Textbox borderDashArray Property
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
            borderDashArray: [5]
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/ca7d7a89c785902e14f8611814eac4d9.png)