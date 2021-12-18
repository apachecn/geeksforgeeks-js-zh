# 织物. js 文本增量属性

> 原文:[https://www . geesforgeks . org/fabric-js-text-deltay-property/](https://www.geeksforgeeks.org/fabric-js-text-deltay-property/)

在本文中，我们将看到如何使用 **Fabric.js** 更改文本画布的 **deltaY** 。画布意味着书写的文本是可移动的、可旋转的、可调整大小的，并且可以拉伸。此外，文本本身不能像文本框一样编辑。

**方法:**为了实现这一点，我们将使用一个名为 **Fabric.js.** 的 JavaScript 库，在使用 CDN 导入库之后，我们将在 body 标签中创建一个画布块，其中将包含我们的文本。之后，我们将初始化 Fabric.js 提供的 canvas 和 Text 实例，并使用 **deltaY** 属性设置 Canvas 文本的 deltaY。

**语法:**

```
fabric.Text(text,
   deltaY: Number
);
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **deltaY:** 它指定了一个指定基线偏移的数字。对于主文本对象，它通常保持为 0。

以下示例说明了**织物. js** 中 **deltaY** 属性的使用:

**示例:**

## 超文本标记语言

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
              width: 400px;">
    <h1 style="color: green;">
      GeeksforGeeks
    </h1>
    <b>
      Fabric.js | Text deltaY Property
    </b>
  </div>
  <div style="text-align: center;">
    <canvas id="canvas"
            width="400" height="200"
      style="border:1px solid green;">
    </canvas>
  </div>
  <script>
    // Create a new instance of Canvas
    var canvas = new fabric.Canvas("canvas");

    // Create a new Text instance
    var geek = new fabric.Text('GeeksforGeeks', {
      deltaY: 0
    });

    // Render the text on Canvas
    canvas.add(geek);
    canvas.centerObject(geek);
  </script>
</body>
</html>
```

**输出:**

![](img/6b98b819305f4bd65e121d8b6adfb911.png)