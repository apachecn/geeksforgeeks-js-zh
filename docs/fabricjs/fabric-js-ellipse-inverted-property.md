# 织物. js 椭圆倒属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellips-inverted-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-inverted-property/)

在本文中，我们将看到如何使用 Fabric.js 设置椭圆画布的反转属性。织物中的椭圆可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个画布块，其中将包含椭圆。之后，我们将初始化由 Fabric.js 提供的 Canvas 和 Ellipse 的实例，并使用反转属性设置 Ellipse 的反转属性，并在 Canvas 上渲染它，如下例所示。

**语法:**

```
fabric.Ellipse({
   rx: number,
   ry: number,
   fill: string,
   inverted: boolean
});
```

**参数:**该函数接受四个参数，如上所述，如下所述:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **填充:**指定填充椭圆的颜色。
*   **反转:**这是一个布尔值，用于设置椭圆的反转属性。

**示例:**本示例使用 Fabric.js 设置画布椭圆的反转属性。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Ellipse inverted Property
    </title>

    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js Ellipse inverted Property
    </h3>

    <canvas id="canvas" width="600" height="300"
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Ellipse instance 
        var ellipse = new fabric.Ellipse({
            rx: 150,
            ry: 75,
            fill: '',
            stroke: 'green',
            inverted: true
        });

        // Render the ellipse in canvas 
        canvas.add(ellipse);
        canvas.centerObject(ellipse);
    </script>
</body>

</html>
```

**输出:**

![](img/fc01923e2f41e178b3c4f860f5e5f561.png)