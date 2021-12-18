# 如何使用 Fabric.js 禁用画布圆的可选择性？

> 原文:[https://www . geeksforgeeks . org/如何禁用-选择-使用织物的画布圈-js/](https://www.geeksforgeeks.org/how-to-disable-selectability-of-a-canvas-circle-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 禁用画布圆圈的可选择性。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以定制该圆。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 circle 实例，并使用**可选**属性禁用 Circle 的可选性，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    selectable: boolean
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定半径。
*   **可选:**指定是否禁用可选性。

**示例:**本示例使用 FabricJS 禁用画布圆的可选择性。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        How to set disable selectability of 
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
            selectable: false
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/af05c8b0bd6822e80ec1dfe6c1c52751.png)