# 织物椭圆 strokeDashOffset 属性

> 原文:[https://www . geesforgeks . org/fabric-js-ellipse-strokedashoffset-property/](https://www.geeksforgeeks.org/fabric-js-ellipse-strokedashoffset-property/)

在本文中，我们将看到如何使用 FabricJS 将笔画偏移设置为画布椭圆。画布椭圆意味着椭圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义椭圆。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含椭圆的主体标签中创建一个画布块。之后，我们将初始化 FabricJS 提供的 canvas 和 Ellipse 的实例，并使用 stroke 属性创建一个笔画，并进一步使用 strokeDashOffset 属性添加笔画偏移，并在 Ellipse 上渲染 Canvas，如下例所示。

**语法:**

```
fabric.Ellipse({
   rx: number,
   ry: number,
   fill: string,
   strokeDashOffset: number
});
```

**参数:**该函数接受四个参数，如上所述，如下所述:

*   **rx:** 指定水平半径。
*   **ry:** 指定垂直半径。
*   **填充:**指定填充椭圆的颜色。
*   **strokeDashOffset:** 指定笔画的偏移量。

**示例:**本示例使用 FabricJS 库将笔画虚线偏移设置为画布椭圆，如下所示。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Ellipse strokeDashOffset Property
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
        Fabric.js Ellipse strokeDashOffset Property
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
            strokeDashArray: [10],
            strokeDashOffset: 10,
            stroke: 'green'
        });

        // Render the ellipse in canvas 
        canvas.add(ellipse);
        canvas.centerObject(ellipse);
    </script>
</body>

</html>
```

**输出:**

![](img/14ed12292eede9f1cf8b2362249a5fdc.png)