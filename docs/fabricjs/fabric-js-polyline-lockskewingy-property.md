# Fabric.js 折线锁定属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-lockskewingy-property/](https://www.geeksforgeeks.org/fabric-js-polyline-lockskewingy-property/)

在本文中，我们将看到如何使用 **FabricJS** 锁定画布折线的垂直倾斜。画布折线是指折线是可移动的，可以根据需要进行拉伸。此外，当涉及初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义折线。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。之后，我们将初始化由**fabrijs**提供的画布和折线实例，并使用 **lockSkewingY** 属性设置画布折线的 lockSkewingY，并在画布上渲染折线，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(
    points, { lockSkewingY: Boolean}
)

```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **点:**保存折线所有点的起点和终点坐标。
*   **lockSkewingY:** 是一个布尔值，指定是否锁定折线画布的垂直倾斜。

以下示例说明了 JavaScript 中的**折线锁定属性**:

**示例:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center;
         width: 600px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Polyline lockSkewingY Property
        </b>
    </div>

    <canvas id="canvas" width="600" height="300" 
        style="border:1px solid #000000;">
    </canvas>

    <script>

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a Polyline instance 
        var polyline = new fabric.Polyline([
            {
                x: 300,
                y: 60
            },
            {
                x: 350,
                y: 100
            }, {
                x: 350,
                y: 230
            }, {
                x: 250,
                y: 230
            }, {
                x: 250,
                y: 100
            }, {
                x: 300,
                y: 60
            }], {

            // Disable skewing
            // along the y-axis
            lockSkewingY: true
        });

        // Render the Polyline in canvas 
        canvas.add(polyline); 
    </script>
</body>

</html>
```

**输出:**

![](img/f89d10f337cbb43bf47db59bdc365aca.png)