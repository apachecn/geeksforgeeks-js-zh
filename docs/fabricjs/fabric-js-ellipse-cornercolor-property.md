# 织物. js |椭圆角颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-corner color-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-cornercolor-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布椭圆控制角的颜色。画布意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个**画布**块，它将包含我们的椭圆。之后，我们将初始化由 FabricJS 提供的 canvas 和 ellipse 的实例，并使用 **cornerColor** 属性设置 Canvas 椭圆的控制角的颜色，并在 Canvas 上渲染 Ellipse，如下例所示。

**语法:**

```
fabric.Ellipse({
    rx: number,
    ry: number,
    cornerColor: string
}); 
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **rx:** 此参数定义水平半径。
*   **ry:** 此参数定义垂直半径。
*   **角颜色:**该参数定义控制角的颜色。

**程序:**本示例使用 FabricJS 设置画布状椭圆的控制角的颜色，如下所示。你必须点击对象才能看到控制角的颜色。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Ellipse cornerColor Property
    </title>

    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <center>
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>
        <b>
            Set color of controlling corners of 
            canvas-type ellipse with JavaScript.
        </b>

        <canvas id="canvas" width="600" height="200" 
            style="border:1px solid #000000">
        </canvas>
    </center>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Ellipse instance
        var ellipse = new fabric.Ellipse({
            rx: 80,
            ry: 40,
            cornerColor: 'red'
        });

        // Render the Ellipse in canvas
        canvas.add(ellipse);
    </script>
</body>

</html>
```

**输出:**
![](img/f119b726edf2e43b606b88a9aad2307b.png)