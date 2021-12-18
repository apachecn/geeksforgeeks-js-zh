# 如何使用 Fabric.js 给画布圆添加阴影？

> 原文:[https://www . geesforgeks . org/如何将阴影添加到画布上-使用织物的圆圈-js/](https://www.geeksforgeeks.org/how-to-add-shadow-to-a-canvas-circle-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 为画布圆添加阴影。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 的实例，并使用 **shadow** 属性为圆形添加阴影，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    shadow: fabric.shadow
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定半径。
*   **阴影:**指定阴影对象。

**示例:**本示例使用 FabricJS 为画布圆添加阴影。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        How to add shadow to a canvas
        circle using FabricJS? 
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

        // Create shadow object
        var shadow = new fabric.Shadow({
            color: 'black',
            blur: 30
        });

        // Initiate a Circle instance
        var circle = new fabric.Circle({
            radius: 50,
            shadow: shadow
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/4b01aec66112778332711db0493a99f6.png)