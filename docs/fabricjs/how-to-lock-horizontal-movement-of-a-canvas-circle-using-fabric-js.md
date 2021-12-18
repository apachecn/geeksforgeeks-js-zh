# 如何使用 Fabric.js 锁定画布圆的水平移动？

> 原文:[https://www . geeksforgeeks . org/如何使用织物锁定画布的水平移动-圆圈-js/](https://www.geeksforgeeks.org/how-to-lock-horizontal-movement-of-a-canvas-circle-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 锁定画布圆圈的水平移动。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以定制该圆。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 的实例，并使用**lockmavementx**属性锁定圆形的水平移动，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    lockMovementX: boolean
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定半径。
*   **lockMovementX:** 指定是否锁定水平移动。

**示例:**本示例使用 FabricJS 锁定画布圆的水平移动。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        How to lock the horizontal movement
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
            lockMovementX: true
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/e8d578b0b27a72d4ee477a145ac2929c.png)