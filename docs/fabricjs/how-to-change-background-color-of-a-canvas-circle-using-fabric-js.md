# 如何使用 Fabric.js 改变画布圆的背景颜色？

> 原文:[https://www . geesforgeks . org/how-change-background-color-of-a-canvas-circle-use-fabric-js/](https://www.geeksforgeeks.org/how-to-change-background-color-of-a-canvas-circle-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 更改画布圆圈的背景颜色。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 实例，并使用 **backgroundColor** 属性更改圆形的背景颜色，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    backgroundColor: string
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定半径。
*   **backgroundColor:** 指定背景颜色。

**示例:**本示例使用 FabricJS 改变画布圆的背景。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        How to change the background of
        canvas circle using FabricJS? 
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
            backgroundColor: 'blue'
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/095ff114228da70d51625a5cddefdd4e.png)