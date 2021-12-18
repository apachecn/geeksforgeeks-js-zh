# 织物. js |三角形填充属性

> 原文:[https://www . geesforgeks . org/fabric-js-triangle-fill-property/](https://www.geeksforgeeks.org/fabric-js-triangle-fill-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布三角形的填充颜色。画布三角形是指三角形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义三角形。
为了实现这一点，我们将使用一个名为**法布里斯**的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含三角形的画布块。之后，我们将初始化 FabricJS 提供的 canvas 和 Triangle 实例，并使用 **fill** 属性设置 Canvas 三角形的填充颜色，并在 Canvas 上渲染三角形，如下例所示。
**语法:**

```
fabric.Triangle({
    width: number,
    height: number,
    fill: string
});

```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定三角形的宽度。
*   **高度:**指定三角形的高度。
*   **填充:**指定填充三角形的颜色。

**示例:**本示例使用 FabricJS 设置画布三角形的填充颜色，如下所示。你必须点击对象才能看到填充颜色。

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Triangle fill Property
    </title>

    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center;width: 600px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Triangle fill Property
        </b>
    </div>
    <canvas id="canvas" width="600" height="300"
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a triangle instance
        var triangle = new fabric.Triangle({
            width: 300,
            height: 150,
            fill: 'blue',
            stroke: 'green',
            strokeWidth: 3
        });

        // Render the Triangle in canvas
        canvas.add(triangle);
        canvas.centerObject(triangle);
    </script>
</body>

</html>
```

**输出:**

![](img/85a0ae9adbd8c403aee7eaff37daa84f.png)