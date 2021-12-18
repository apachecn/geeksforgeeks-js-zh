# Fabric.js Circle flipX 属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-flipx-property/](https://www.geeksforgeeks.org/fabric-js-circle-flipx-property/)

在本文中，我们将看到如何使用 Fabric.js 水平翻转一个圆。Fabric.js 中的圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或大小时，可以自定义圆形。

**方法:**为了使其成为可能，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在 body 标记中创建一个画布块，其中将包含 Circle。之后，我们将初始化 Fabric.js 提供的 Canvas 和 circle 的实例，设置是否使用 flipX 属性水平翻转 Circle，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   flipX: boolean
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **flipX:** 指定是否水平翻转对象。

**示例:**本示例使用 Fabric.js 水平翻转画布圆。

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
        Fabric.js Circle flipX Property
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
            fill: '',
            stroke: 'green',
            strokeWidth: 3,
            flipY: true
        });

        // Render the circle in canvas 
        canvas.add(circle);
        canvas.centerObject(circle);
    </script>
</body>
</html>
```

**输出:**

![](img/85cf65b453d2a48890bc5daf67a4f9f2.png)