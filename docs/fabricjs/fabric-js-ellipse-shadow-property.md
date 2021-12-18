# Fabric.js |椭圆阴影属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-shadow-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-shadow-property/)

在本文中，我们将看到如何使用 FabricJS 为画布椭圆添加阴影。画布意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个**画布**块，它将包含我们的椭圆。之后，我们将初始化由 FabricJS 提供的 canvas 和 Ellipse 的实例，并使用**阴影**属性向 Canvas 椭圆添加阴影，并在 Canvas 上渲染椭圆，如下例所示。

**语法:**

```
fabric.Ellipse({
    rx: number,
    ry: number,
    shadow: fabric.shadow
}); 
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **阴影:**指定阴影对象。

**示例:**本示例使用 FabricJS 为画布椭圆添加阴影。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        Fabric.js | Ellipse shadow Property
    </title>

    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center;width: 600px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Ellipse shadow Property
        </b>
    </div>

    <div style="text-align: center;">
    <canvas id="canvas" width="600" height="200" 
            style="border:1px solid #000000;">
    </canvas>
    </div>

    <script>
        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Create shadow object
        var shadow = new fabric.Shadow({
            color: 'black',
            blur: 30
        });

        // Initiate a Ellipse instance
        var ellipse = new fabric.Ellipse({
            rx: 80,
            ry: 50,
            shadow: shadow
        });

        // Render the Ellipse in canvas
        canvas.add(ellipse);
    </script>
</body>

</html>                   
```

**输出:**
![](img/ca119f1bf6b2a4c7a8e1ea673ab84f41.png)