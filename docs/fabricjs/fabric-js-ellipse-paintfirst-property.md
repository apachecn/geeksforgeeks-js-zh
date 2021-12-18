# 织物. js 椭圆涂料第一属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-paint first-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-paintfirst-property/)

在本文中，我们将看到如何使用 FabricJS 更改画布 Textbox 的 paintFirst 属性。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含文本框的画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 paintFirst 属性更改 Textbox 的 paint first 属性值，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Ellipse({
   rx: number,
   ry: number,
   fill: string,
   paintFirst: string
});
```

**参数:**该函数接受四个参数，如上所述，如下所述:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **填充:**指定填充椭圆的颜色。
*   **paintFirst:** 指定 paintFirst 属性的字符串值。

**示例:**本示例使用 FabricJS 设置画布椭圆的 paintFirst 属性。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Ellipse paintFirst Property
    </title>

    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js Ellipse paintFirst Property
    </h3>

    <canvas id="canvas" width="600" height="300"
        style="border:1px solid #000000">
    </canvas>

    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Ellipse instance 
        var ellipse = new fabric.Ellipse({
            rx: 150,
            ry: 75,
            fill: 'green',
            stroke: 'blue',
            paintFirst: 'fill'
        });

        // Render the ellipse in canvas 
        canvas.add(ellipse);
        canvas.centerObject(ellipse);
    </script>
</body>

</html>
```

**输出:**

![](img/590ba685dea0655fa69ebcd561be9bf8.png)