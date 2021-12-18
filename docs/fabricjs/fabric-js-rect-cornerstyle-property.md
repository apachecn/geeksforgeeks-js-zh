# Fabric.js | Rect cornerStyle 属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-corner style-property/](https://www.geeksforgeeks.org/fabric-js-rect-cornerstyle-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布矩形的控制角的样式。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Rectangle 的实例，并使用 cornerStyle 属性设置 Canvas 矩形的控制角的样式，并在 Canvas 上呈现矩形，如下例所示。
**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    cornerStyle: string
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **转角样式:**指定控制转角的样式。这个参数的接受值是圆形和矩形。

**示例:**本示例使用 FabricJS 设置画布状矩形的控制角的样式，如下所示。你必须点击对象才能看到控制角的样式。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Rect cornerStyle Property
    </title>

    <!-- Adding the FabricJS library -->
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

        // Initiate a Rect instance
        var rectangle = new fabric.Rect({
            width: 200,
            height: 100,
            fill: '',
            stroke: 'green',
            strokeWidth: 3,
            cornerStyle: 'circle'
        });

        // Render the Rect in canvas
        canvas.add(rectangle);
        canvas.centerObject(rectangle);
    </script>
</body>

</html>
```

**输出:**

![](img/26527195d2edc458a83db5e35132e251.png)