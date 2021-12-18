# fabric . js | Circle has controls Property

> 原文:[https://www . geesforgeks . org/fabric-js-circle-has controls-property/](https://www.geeksforgeeks.org/fabric-js-circle-hascontrols-property/)

在本文中，我们将看到如何使用 FabricJS 禁用画布圆圈的操作。画布意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以对圆进行自定义。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含我们的圆的*画布*块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 circle 实例，并使用 **hasControls** 属性禁用对 Circle 的操作，并在 Canvas 上渲染 Circle，如下例所示。

**语法:**

```
fabric.Circle({
    radius: number,
    hasControls: boolean
}); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **有控制:**指定是否禁用控制。

**示例:**本示例使用 FabricJS 禁用画布圆的操纵。注意你必须点击物体才能看到角落。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Circle hasControls Property
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
            hasControls: false
        });

        // Render the circle in canvas
        canvas.add(circle);
    </script>
</body>

</html>
```

**输出:**
![](img/28377dace27c16c9d6cbdc8d1d1ec363.png)