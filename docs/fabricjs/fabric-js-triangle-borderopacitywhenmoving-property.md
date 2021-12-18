# 移动属性时的三角形边框

> 原文:[https://www . geesforgeks . org/fabric-js-triangle-borderopacitywhen moveing-property/](https://www.geeksforgeeks.org/fabric-js-triangle-borderopacitywhenmoving-property/)

在本文中，我们将看到如何绘制一个画布三角形，当用户使用 **FabricJS** 移动三角形时，该三角形的边框不透明度将会改变。画布三角形是指三角形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充或笔画宽度时，可以自定义三角形。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含三角形的画布块。之后，我们将初始化由 **FabricJS** 提供的画布和三角形的实例，并使用**borderropacitywhen movement**属性启用画布三角形的 borderropacitywhen movement，并在画布上渲染三角形，如下所示。

**语法:**

```
fabric.Triangle({
    width: number,
    height: number,
    borderOpacityWhenMoving: number
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定三角形的宽度。
*   **高度:**指定三角形的高度。
*   **边界多边形移动时:**此参数定义三角形的边界不透明度。

**示例:**该示例使用 **FabricJS** 来启用如下所示的画布状三角形移动时的 borderopacity。在启用**边框属性后移动对象时尝试边框属性当移动**属性时，它将按定义的数字更改三角形边框的不透明度。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Triangle borderOpacityWhenMoving Property
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
            Fabric.js | Triangle borderOpacityWhenMoving Property
        </b>
        </div>
    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance
        var canvas = new fabric.Canvas("canvas");

        // Initiate a triangle instance
        var triangle = new fabric.Triangle({
                        width: 150,
                        height: 100,
                        fill: '',
                        stroke: 'green',
                        strokeWidth: 3,
                        cornerColor: 'blue',
                        borderOpacityWhenMoving: 0.2
        });

        // Render the triangle in canvas
        canvas.add(triangle);
        canvas.centerObject(triangle);
    </script>
</body>

</html>                   
```

**输出:**

![](img/edcd22412ef6e19dbfeaa7cf7a8eb199.png)