# 织物. js 组高度属性

> 原文:[https://www . geesforgeks . org/fabric-js-group-height-property/](https://www.geeksforgeeks.org/fabric-js-group-height-property/)

下面的文章介绍了如何使用 **Fabric.js** 设置画布的**组**的**高度**。Fabric.js 中的组是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义该组。

为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在包含组的主体标签中创建画布块。之后，我们将初始化 **Fabric.js** 提供的 Canvas 和 Group 的实例，并使用 **height** 属性设置 Group 的高度。

**语法:**

```
fabric.Group([canvas1, canvas2], {
   height: Number
});
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **高度:**指定物体的高度。

以下示例说明了在 JavaScript 中使用 Fabric.js 组**高度**属性:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <!-- FabricJS CDN -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>
<body>
    <div style="text-align: center;width: 400px;">
      <h1 style="color: green;">
          GeeksforGeeks
      </h1>
      <b>
          Fabric.js | Group height Property
      </b>
    </div>

    <div style="text-align: center;">
      <canvas id="canvas" width="500" height="300"
      style="border:1px solid green;">
      </canvas>
    </div>

    <script>
      // Initiate a Canvas instance
      var canvas = new fabric.Canvas("canvas");

      // Initiate a circle instance
      var circle = new fabric.Circle({
        radius: 100,
        fill: 'lightgreen',
        scaleY: 0.6,
        originX: 'center',
        originY: 'center'
      });

      // Initiate a text instance
      var text = new fabric.Text('GeeksforGeeks', {
        fontSize: 25,
        originX: 'center',
        originY: 'center'
      });

      // Initiate a Group instance
      var group = new fabric.Group([ circle, text ], {
        height: 50 
      });

      // Render the Group in canvas
      canvas.add(group);

      // Center the Group in canvas
      canvas.centerObject(group);
  </script>
</body>
</html>
```

**输出:**

![](img/c27513b18e93cb74680d3251fbd36e90.png)