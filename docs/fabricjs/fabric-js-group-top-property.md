# 织物 js 集团顶级物业

> 原文:[https://www.geeksforgeeks.org/fabric-js-group-top-property/](https://www.geeksforgeeks.org/fabric-js-group-top-property/)

在本文中，我们将看到如何使用 **Fabric.js** 设置画布的**组**的**顶部**。Fabric.js 中的组是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义该组。

**进场:**

*   为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript HTML5 画布库。
*   导入库后，我们将在主体标签中创建一个包含组的画布块。
*   之后，我们将初始化 Fabric.js 提供的 Canvas 和 Group 的实例，并使用 **top** 属性设置相对于 canvas Group 中顶部的位置。

**语法:**

```
fabric.Group([canvas1, canvas2], {
   top: Number
});
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **顶部:**指定相对于画布组顶部的位置。它包含一个数值。

以下示例说明了在 JavaScript 中使用 Fabric.js Group **top** 属性:

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
          Fabric.js | Group top Property
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
        top: 150
      });

      // Render the Group in canvas
      canvas.add(group);
  </script>
</body>

</html>
```

**输出:**

![](img/1f02a273b9bd2e4bb32bb1bfa86159f2.png)