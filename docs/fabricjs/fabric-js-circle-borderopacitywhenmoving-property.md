# 移动属性时的圆形边界

> 原文:[https://www . geesforgeks . org/fabric-js-circle-borderopacitywhen moveing-property/](https://www.geeksforgeeks.org/fabric-js-circle-borderopacitywhenmoving-property/)

在本文中，我们将看到如何在使用 FabricJS 移动画布圆时更改边框不透明度。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在 body 标签中创建一个包含我们的圆的**画布**块。在这之后，我们将初始化由 FabricJS 提供的 Canvas 和 Circle 的实例，并在使用**borderropacity 当移动**属性移动圆形时更改边框不透明度，并在 Canvas 上渲染圆形，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    borderOpacityWhenMoving: number
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **移动时边框的不透明度:**指定移动时边框的不透明度。默认值为 0.4。

**示例:**本示例使用 FabricJS 在移动画布圆的同时更改边框不透明度。请注意，您必须单击对象才能看到边框。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Circle borderOpacityWhenMoving Property
    </title>

    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <center>
        <h1 style="Color: green;">
            GeeksforGeeks
        </h1>

        <b>
            Change border opacity while moving 
            a canvas circle using FabricJS.
        </b>

        <canvas id="canvas" width="600" height="200" 
            style="border:1px solid #000000">
        </canvas>

        <script>

            // Initiate a Canvas instance
            var canvas = new fabric.Canvas("canvas");

            // Initiate a Circle instance
            var circle = new fabric.Circle({
                radius: 50,
                borderOpacityWhenMoving: 1
            });

            // Render the circle in canvas
            canvas.add(circle);
        </script>
    </center>
</body>

</html>
```

**输出:**
![](img/a2735d749da71fdc8539ccf21dbd1be6.png)