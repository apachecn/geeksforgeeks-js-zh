# 移动属性时的织物线边界

> 原文:[https://www . geesforgeks . org/fabric-js-line-borderopacitywhen moveing-property/](https://www.geeksforgeeks.org/fabric-js-line-borderopacitywhenmoving-property/)

在本文中，我们将看到如何绘制一条画布线，当用户使用 **【法布里斯】** 移动线条时，该画布线的边框不透明度将发生变化。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

**语法:**

```html
fabric.line({
    borderOpacityWhenMoving : Number
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化 **FabricJS** 提供的 canvas 和线条的实例，并使用**borderropacitywhealing**属性设置移动时 Canvas 线条的边框不透明度，并在 Canvas 上渲染线条，如下所示。**

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **移动时边框的不透明度:**它指定移动时边框的不透明度，该参数取值范围为 0 到 1。它包含一个数字值。

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
    <h1>
        fabric.js | line borderOpacityWhenMoving property
    </h1>

    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000;"> 
    </canvas>

    <script>
        var canvas = new fabric.Canvas("canvas");

        var line = new fabric.Line([150, 10, 220, 150], {
            stroke: 'green',
            borderOpacityWhenMoving: 0
        });

        canvas.add(line);
    </script>
</body>

</html>
```

**输出:**

![](img/37b15398b429a26df0530593f62d41c9.png)

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
    <h1>
        fabric.js | line borderOpacityWhenMoving property
    </h1>

    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000;"> 
    </canvas>

    <script>
        var canvas = new fabric.Canvas("canvas");

        var line = new fabric.Line([150, 10, 220, 150], {
            stroke: 'green',
            borderOpacityWhenMoving: 0.2
        });

        canvas.add(line);
    </script>
</body>

</html>
```

**输出:**

![](img/6ec82e50ca6308dc6ae5445c3837377e.png)