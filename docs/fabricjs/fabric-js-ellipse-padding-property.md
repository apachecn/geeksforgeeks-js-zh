# 织物. js |椭圆填充属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-padding-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-padding-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布椭圆的填充，以便保持对象的纵横比。画布意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。
为了实现这一点，我们将使用一个名为**法布里斯**的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的椭圆的**画布**块。之后，我们将初始化 **FabricJS** 提供的画布和椭圆的实例，并使用**填充**属性设置画布椭圆的填充，并在画布上渲染椭圆，如下例所示。
**语法:**

```
fabric.Ellipse({
    rx: number,
    ry: number,
    padding: number
}); 
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **填充:**此参数指定填充。

**示例:**本示例使用 FabricJS 设置画布椭圆的填充。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Ellipse padding Property
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
            Fabric.js | Ellipse padding Property
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

        // Initiate a Ellipse instance
        var ellipse = new fabric.Ellipse({
            rx: 80,
            ry: 40,
            padding: 30
        });

        // Render the Ellipse in canvas
        canvas.add(ellipse);
    </script>
</body>

</html>                  
```

**输出:**

![](img/c2bceee5cb8f32f61a8da6af2d5e57f0.png)