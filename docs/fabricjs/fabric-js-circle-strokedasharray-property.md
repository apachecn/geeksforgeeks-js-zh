# 布艺. js |圆形 strokeDashArray 属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-strokedasharray-property/](https://www.geeksforgeeks.org/fabric-js-circle-strokedasharray-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布圆的笔画划线模式。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以定制该圆。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 实例，并分别使用**描边**和**描边**属性设置圆形的描边颜色和描边虚线图案，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    stroke: string,
    strokeDashArray: array
}); 

```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **笔画:**指定笔画颜色。
*   **strokeDashArray:** 指定笔画破折号模式。

**示例:**本示例使用 FabricJS 设置画布圆的描边破折号图案。

```
<!DOCTYPE html>
<html>

<head>
    <title> 
        Fabric.js | Circle strokeDashArray Property
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
            Set stroke dash pattern of a canvas
            circle using FabricJS
        </b>

        <canvas id="canvas" width="600" height="200" 
            style="border:1px solid #000000">
        </canvas>
    </center>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Circle instance
        var circle = new fabric.Circle({
            radius: 50,
            stroke: "red",
            strokeDashArray: [10]
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**

![](img/9732024711420dc3453a7da4588aa6d0.png)