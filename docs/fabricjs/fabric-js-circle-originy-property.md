# 织物. js 圆原点属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-originy-property/](https://www.geeksforgeeks.org/fabric-js-circle-originy-property/)

在本文中，我们将看到如何使用 Fabric.js 设置对象画布圆的变换的垂直原点。Fabric.js 中的圆是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或大小时，可以自定义圆形。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含圆圈的画布块。之后，我们将初始化 Fabric.js 提供的 Canvas 和 Circle 的实例，使用 originY 属性设置圆形的垂直变换，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   originY: string
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **originY:** 指定圆的垂直变换。

**示例:**本示例使用 Fabric.js 设置圆的垂直变换。

## 超文本标记语言

```
<!DOCTYPE html>
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
        Fabric.js Circle originY Property
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
            originY: "center"
        });

        // Render the circle in canvas 
        canvas.add(circle);
    </script>
</body>
</html>
```

**输出:**

![](img/175e21dc45a9b7d047278e6ed54af69d.png)