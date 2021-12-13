# Fabric.js 多边形 noScaleCache 属性

> 原文:[https://www . geesforgeks . org/fabric-js-polygon-no scale cache-property/](https://www.geeksforgeeks.org/fabric-js-polygon-noscalecache-property/)

在本文中，我们将看到使用 FabricJS 的多边形画布的 noScaleCache 属性。画布多边形意味着多边形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义多边形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含多边形的画布块。在这之后，我们将初始化由 FabricJS 提供的 canvas 和多边形的实例，并使用 noScaleCache 属性设置 Canvas 多边形的 noScaleCache，并在 Canvas 上渲染多边形，如下例所示。

**语法:**

```html
fabric.Polygon([
    { x: pixel, y: pixel },
    { x: pixel, y: pixel },
    { x: pixel, y: pixel},
    { x: pixel, y: pixel},
    { x: pixel, y: pixel }
],
{
    noScaleCache: boolean
});
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **无缓存:**当“真”时，对象被缓存在一个额外的画布上。当“false”时，除非必要，否则不缓存对象(clipPath)默认为 true。

下面的例子说明了织物。JavaScript 中的 JS 多边形无级缓存:

**示例:**

## 超文本标记语言

```html
<!DOCTYPE html> 
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
        Fabric.js | Polygon noScaleCache Property 
    </b> 
  </div> 

  <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
  </canvas> 

  <script> 
    // Initiate a Canvas instance 
    var canvas = new fabric.Canvas("canvas"); 

    // Initiate a polygon instance 
    var polygon = new fabric.Polygon([ 
        { x: 295, y: 10 }, 
        { x: 235, y: 198 }, 
        { x: 385, y: 78 }, 
        { x: 205, y: 78 }, 
        { x: 355, y: 198 }], { 
         noScaleCache: 'true' 

    }); 

    // Render the polygon in canvas 
    canvas.add(polygon); 
  </script> 
</body> 

</html>
```

**输出:**

![](img/41edeb804dcbb04c7e6f1be3eb936faf.png)