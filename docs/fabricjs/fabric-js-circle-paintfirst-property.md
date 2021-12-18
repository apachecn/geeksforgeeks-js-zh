# 布艺. js 圆画第一属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-paint first-property/](https://www.geeksforgeeks.org/fabric-js-circle-paintfirst-property/)

在本文中，我们将看到如何使用 Fabric.js 更改画布圆的 paintFirst 属性。Fabric.js 中的圆是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或大小时，可以自定义圆形。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个画布块，其中将包含 Circle。之后，我们将初始化 Fabric.js 提供的 Canvas 和 Circle 的实例，使用 paintFirst 属性更改 Circle 的 paint first 属性值，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   paintFirst: string
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **paintFirst:** 指定是先画对象的填充还是先画对象的描边。它可以是“填充”或“描边”。

**示例:**本示例使用 Fabric.js 设置画布圆的 paintFirst 属性。

## 超文本标记语言

```
<html>
<head>
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
        Fabric.js Circle paintFirst Property
    </h3>
    <canvas id="canvas" width="600" height="300" 
            style="border:1px solid #000000">
    </canvas>
    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Circle instance 
        var circle = new fabric.Circle({
            radius: 100,
            fill: 'green',
            stroke: 'blue',
            strokeWidth: 3,
            paintFirst: 'fill'
        });

        // Render the circle in canvas 
        canvas.add(circle);
        canvas.centerObject(circle);
    </script>
</body>
</html>
```

**输出:**

![](img/6ce297d271662bcf76945630e45dc8e2.png)