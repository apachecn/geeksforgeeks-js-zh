# 织物|三角形原点属性

> 原文:[https://www . geesforgeks . org/fabric-js-triangle-originy-property/](https://www.geeksforgeeks.org/fabric-js-triangle-originy-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置对象画布三角形变换的垂直原点。画布三角形是指三角形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义三角形。
为了实现这一点，我们将使用一个名为**法布里斯**的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含三角形的画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和三角形的实例，并使用 **originY** 属性设置三角形的垂直变换，并在 Canvas 上渲染三角形，如下例所示。
**语法:**

```
fabric.Triangle({
    width: number,
    height: number,
    originY: string
});

```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定三角形的宽度。
*   **高度:**指定三角形的高度。
*   **originY:** 指定画布三角形的垂直变换。

**示例:**本示例使用 FabricJS 设置画布三角形的垂直变换。

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Triangle originY Property
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
            Fabric.js | Triangle originY Property 
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
            fill: '',
            stroke: 'green',
            strokeWidth: 3,
            originY: 'center'
        });

        // Render the Triangle in canvas
        canvas.add(triangle);
    </script>
</body>

</html>
```

**输出:**

![](img/db98bfda09c820ac62d1f873ca58b243.png)