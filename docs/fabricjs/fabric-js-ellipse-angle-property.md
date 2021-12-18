# 织物椭圆角度属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-angle-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-angle-property/)

在本文中，我们将看到如何使用 FabricJS 绘制一个固定角度的画布椭圆。画布椭圆意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义椭圆。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript HTML5 画布库。
*   导入库后，我们将在包含椭圆的主体标签中创建一个画布块。
*   之后，我们将初始化由 FabricJS 提供的 canvas 和 Ellipse 的实例，并使用 angle 属性启用 canvas Ellipse 的角度，并在 Canvas 上渲染 Ellipse，如下所示。

**语法:**

```
fabric.Ellipse({
   rx: number,
   ry: number,
   fill: string,
   angle: number
});
```

**参数:**该函数接受四个参数，如上所述，如下所述:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **填充:**指定填充椭圆的颜色。
*   **角度:**该参数定义椭圆的角度。

**示例:**本示例使用 FabricJS 启用画布状椭圆的角度，如下所示。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Ellipse angle Property
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
        Fabric.js Ellipse angle Property
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
            fill: '',
            stroke: 'green',
            angle: 45
        });

        // Render the ellipse in canvas 
        canvas.add(ellipse);
        canvas.centerObject(ellipse);
    </script>
</body>

</html>
```

**输出:**

![](img/da5494ccae6c7e49bd3d9b41632f9585.png)