# 如何使用 Fabric.js 缩放控制画布圆的边框？

> 原文:[https://www . geeksforgeeks . org/如何缩放-使用织物控制画布圈边框-js/](https://www.geeksforgeeks.org/how-to-scale-controlling-border-of-a-canvas-circle-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 缩放画布圆的控制边框。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以定制该圆。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Circle 的实例，并使用 **borderScaleFactor** 属性来缩放控制圆形的边框，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    borderScaleFactor: number
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定半径。
*   **边框缩放因子:**指定控制边框的大小。

**示例:**本示例使用 FabricJS 缩放画布圆的控制边框。请注意，您必须单击对象才能看到边框。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to scale controlling border of
        a canvas circle using FabricJS?
    </title>

    <!-- FabricJS CDN -->
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

        // Initiate a Circle instance
        var circle = new fabric.Circle({
            radius: 50,
            borderScaleFactor: 5
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/0abd8064208ca21944effa83cc7a83bc.png)