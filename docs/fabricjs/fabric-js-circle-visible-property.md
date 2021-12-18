# 织物. js 圆可见属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-visible-property/](https://www.geeksforgeeks.org/fabric-js-circle-visible-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布圆的可见性。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或大小时，可以自定义圆形。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript HTML5 画布库。
*   使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的圆形。
*   之后，我们将初始化由 FabricJS 提供的 canvas 和 Circle 的实例，并使用 visible 属性设置 canvas Circle 的可见性，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   visible: boolean
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **可见:**指定对象的可见性。

**示例:**本示例使用 FabricJS 设置画布圆的可见性。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Circle visible Property
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
        Fabric.js Circle visible Property
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
            visible: false
        });

        // Render the circle in canvas 
        canvas.add(circle);
        canvas.centerObject(circle);
    </script>
</body>

</html>
```

**输出:**

![](img/3f30a72577f0748b646f9dfb99ec293a.png)