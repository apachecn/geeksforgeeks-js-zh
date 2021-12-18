# 织物. js |圆角颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-corner color-property/](https://www.geeksforgeeks.org/fabric-js-circle-cornercolor-property/)

在本文中，我们将看到如何使用 FabricJS 更改画布圆的控制角颜色。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在 body 标签中创建一个包含我们的圆的**画布**块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 实例，并使用 **cornerColor** 属性更改圆形的控制角颜色，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    cornerColor: string
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**此参数保存圆的半径。
*   **角颜色:**该参数指定控制角的颜色。

**示例:**本示例使用 FabricJS 更改画布圆的控制角颜色。请注意，您必须单击对象才能看到颜色。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Circle cornerColor Property
    </title>

    <!-- FabricJS CDN -->
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
            Change the controlling corners color of
            canvas circle using FabricJS
        </b>

        <canvas id="canvas" width="600" height="200"
            style="border:1px solid #000000">
        </canvas>

        <script>

            // Initiate a Canvas instance
            var canvas = new fabric.Canvas("canvas");

            // Initiate a Circle instance
            var circle = new fabric.Circle({
                radius: 50,
                cornerColor: 'green'
            });

            // Render the circle in canvas
            canvas.add(circle);
        </script>
    </center>
</body>

</html>
```

**输出:**
![](img/4ab99f56c0cccd29666589e25d398af3.png)