# 织物. js |椭圆边界比例因子属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-ellipse-borderscale factor-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-borderscalefactor-property/)

在本文中，我们将看到如何使用 FabricJS 缩放画布椭圆的控制边框。画布意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的椭圆的*画布*块。之后，我们将初始化由 FabricJS 提供的画布和椭圆的实例，并使用**边界缩放因子**属性缩放画布椭圆的控制边界，并在画布上渲染椭圆，如下例所示。

**语法:**

```
fabric.Ellipse({
    rx: number,
    ry: number,
    borderScaleFactor: number
}); 
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **边框比例因子:**指定控制边框的比例因子。

**程序:**本示例使用 FabricJS 缩放画布状椭圆的控制边框，如下所示。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Ellipse borderScaleFactor Property
    </title>

    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Ellipse instance
        var ellipse = new fabric.Ellipse({
            rx: 80,
            ry: 40,
            borderScaleFactor: 3
        });

        // Render the Ellipse in canvas
        canvas.add(ellipse);
    </script>
</body>

</html>
```

**输出:**
![](img/2d17c68e2e8652aaede1a4c39a3dccd3.png)