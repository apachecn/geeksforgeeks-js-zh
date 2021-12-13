# 织物. js 线 borderDashArray 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-line-bordersharray-property/](https://www.geeksforgeeks.org/fabric-js-line-borderdasharray-property/)

在本文中，我们将看到如何使用 **FabricJS** 来设置画布线条边框的破折号图案。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

**语法:**

```html
fabric.line({
    borderDashArray: Array
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化**fabrijs**提供的 canvas 和线条的实例，并使用**bordersharray**属性设置 Canvas 线条的边框虚线图案，并在 Canvas 上渲染该线条，如下所示。**

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **bordersharray:**指定对象边框的破折号图案。

**例 1:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1>fabric.js | line borderDashArray property</h1>

    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000;"> 
    </canvas>

    <script>
        var canvas = new fabric.Canvas("canvas");

        var line = new fabric.Line([150, 10, 220, 150], {
            stroke: 'green',
            borderDashArray: [10]
        });

        canvas.add(line);
    </script>
</body>

</html>
```

**输出:**

![](img/c5bc1a18802fe0153d7ab89f03bc13c2.png)

**例 2:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1>fabric.js | line borderDashArray property</h1>

    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000;"> 
    </canvas>

    <script>
        var canvas = new fabric.Canvas("canvas");

        var line = new fabric.Line([150, 10, 220, 150], {
            stroke: 'green',
            borderDashArray: [4]
        });

        canvas.add(line);
    </script>
</body>

</html>
```

**输出:**

![](img/abb4c5f52440e44e3e38699cd64c3e22.png)