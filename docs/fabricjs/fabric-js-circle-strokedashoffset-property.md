# 织物. js 圆形 strokeDashOffset 属性

> 原文:[https://www . geesforgeks . org/fabric-js-circle-strokedashoffset-property/](https://www.geeksforgeeks.org/fabric-js-circle-strokedashoffset-property/)

在本文中，我们将看到如何使用 FabricJS 将笔画虚线偏移设置为画布圆形。画布圆意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义圆形。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript HTML5 画布库。
*   导入库后，我们将在主体标签中创建一个包含圆形的画布块。
*   之后，我们将初始化 FabricJS 提供的 canvas 和 Circle 的实例，并使用 stroke 属性创建一个笔画，并进一步使用 strokeDashOffset 属性添加笔画偏移，并在 Circle 上渲染 Canvas，如下例所示。

**语法:**

```
fabric.Circle({
   radius: number,
   stroke: string,
   strokeDashOffset: number
});
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **半径:**指定圆的半径。
*   **笔画:**指定笔画颜色。
*   **strokeDashOffset:** 指定笔画的偏移量。

**示例:**本示例使用 FabricJS 库设置画布圆的描边虚线偏移，如下所示。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js Circle strokeDashOffset Property
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
        Fabric.js Circle strokeDashOffset Property
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
            strokeDashArray: [10],
            strokeDashOffset: 5
        });

        // Render the circle in canvas 
        canvas.add(circle);
        canvas.centerObject(circle);
    </script>
</body>

</html>
```

**输出:**

![](img/ac954b2e5904e822f77108c4e483f0ec.png)