# 织物. js |圆形不透明度属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-不透明度-property/](https://www.geeksforgeeks.org/fabric-js-circle-opacity-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布圆的不透明度。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Circle 实例，并使用**不透明度**属性设置圆形的不透明度，并在 Canvas 上渲染圆形，如下例所示。
**语法:**

```
fabric.Circle({
    radius: number,
    opacity: number
});
```

**参数:**该功能接受两个参数，如上所述，描述如下:

*   **半径:**指定圆的半径。
*   **不透明度:**指定圆形画布的不透明度。

**示例:**本示例使用 FabricJS 设置画布圆的不透明度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Circle opacity Property
    </title>

    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Circle instance
        var circle = new fabric.Circle({
            radius: 50,
            opacity: 1
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**

![](img/3dd20752877f0cb61da8906d201df341.png)