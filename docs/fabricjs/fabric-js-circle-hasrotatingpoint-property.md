# 织物. js |圆有旋转点属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-hasrotating point-property/](https://www.geeksforgeeks.org/fabric-js-circle-hasrotatingpoint-property/)

在本文中，我们将看到如何使用 FabricJS 禁用画布圆的旋转。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 circle 实例，并使用**的 hasRotatingPoint** 属性禁用 Circle 的旋转，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    hasRotatingPoint: boolean
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **有旋转点:**指定是否禁用旋转控制。

**示例:**本示例使用 FabricJS 禁用画布圆的旋转。注意你必须点击物体才能看到角落。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        Fabric.js | hasRotatingPoint Property
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
            hasRotatingPoint: false
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/e32928a0fa1adc6e1e12fa13b2f0bc56.png)