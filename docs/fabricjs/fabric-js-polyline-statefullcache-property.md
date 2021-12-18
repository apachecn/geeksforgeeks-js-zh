# Fabric.js 折线状态全缓存属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-statefullcache-property/](https://www.geeksforgeeks.org/fabric-js-polyline-statefullcache-property/)

在本文中，我们将使用 Fabric.js 查看折线的 statefullCache 属性。Fabric.js 中的折线是可移动的，并且可以根据 g 到要求进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义折线。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含折线的画布块。之后，我们将初始化 Fabric.js 提供的 Canvas 和 Polyline 的实例，设置是否使用 statefullCache 属性检查对象属性的缓存失效，并在 Canvas 上渲染 Polyline，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, {  
    statefullCache : boolean
 });  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **statefullCache:** 是一个布尔值，它指定对象的属性是否被检查缓存无效。

以下示例说明了 Fabric.js 中的 statefullCache 属性:

**示例:**

## 超文本标记语言

```
<html>
<head>
  <!-- Loading the FabricJS library -->
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
      Fabric.js | Polyline statefullCache Property
    </b>
  </div>
  <canvas id="canvas" width="600" height="200" 
          style="border:1px solid #000000;">
  </canvas>
  <script>

    // Initiate a Canvas instance 
    var canvas = new fabric.Canvas("canvas");

    // Initiate a polyline instance 
    var polyline = new fabric.Polyline([
      {
        x: 200,
        y: 10
      }, {
        x: 250,
        y: 50
      }, {
        x: 250,
        y: 180
      }, {
        x: 150,
        y: 180
      }, {
        x: 150,
        y: 50
      }, {
        x: 200,
        y: 10
      }], {
      stroke: 'green',
      strokeWidth: 3,
      fill: 'yellow',
      statefullCache: 'false'
    });

    // Render the polyline in canvas 
    canvas.add(polyline); 
  </script>
</body>
</html>
```

**输出:**

![](img/3eb2edb29abbae1fe71ae1a47a001d10.png)