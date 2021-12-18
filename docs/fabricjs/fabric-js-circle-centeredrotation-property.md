# 织物. js 圆中心位置属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-centere station-property/](https://www.geeksforgeeks.org/fabric-js-circle-centeredrotation-property/)

在本文中，我们将看到如何使用 **FabricJS** 来启用/禁用画布圆的居中旋转。画布圆是指圆是可移动的，可以根据需要拉伸。此外，当涉及到初始*笔画颜色、填充颜色、笔画宽度、*或*半径时，可以自定义圆圈。*

**方法:**为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的圆。之后，我们将初始化由**fabrijs**提供的画布和圆的实例，并使用*centereprotation*属性取消画布圆的居中旋转，并在画布上渲染圆，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   centeredRotation: boolean
});
```

**参数:**该函数接受两个参数，如上所述，如下所述。

*   **半径:**指定圆的半径。
*   **居中旋转:**指定是启用还是禁用居中旋转。

**示例:**本示例使用 **FabricJS** 来启用/禁用画布状圆圈的居中旋转，如下所示。尝试在启用/禁用居中旋转后旋转对象，它将使用左上角作为旋转中心。

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
        Fabric.js Circle centeredRotation Property
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
            centeredRotation: false
        });

        // Render the circle in canvas 
        canvas.add(circle);
        canvas.centerObject(circle);
    </script>
</body>

</html>
```

**输出:**

![](img/be2442e22d6bc88effdff223845c2687.png)