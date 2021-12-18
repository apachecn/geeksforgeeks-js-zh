# 织物. js 折线左侧属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-left-property/](https://www.geeksforgeeks.org/fabric-js-polyline-left-property/)

在本文中，我们将看到如何使用 FabricJS 设置折线画布的左侧属性。画布折线意味着折线是可移动的，可以根据需要拉伸。此外，在初始描边颜色、高度、宽度、填充颜色或描边宽度方面，可以自定义折线。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。在此之后，我们将初始化由 FabricJS 提供的 canvas 和 Polyline 的实例，并设置 Canvas 的 left 属性的值，并在 Canvas 上渲染 Polyline，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, {  
   left: number
});  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **左侧:**指定对象的左侧位置。

以下示例说明了 Fabric.js 中的左侧属性:

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
  <div style="text-align: center;width: 600px;"> 
    <h1 style="color: green;"> 
        GeeksforGeeks 
    </h1> 
    <b> 
        Fabric.js | Polyline left Property 
    </b> 
  </div> 

  <canvas id="canvas"
    width="600"
    height="200"
    style="border:1px solid #000000;"> 
  </canvas> 

  <script> 
    // Initiate a Canvas instance 
    var canvas = new fabric.Canvas("canvas"); 

    // Initiate a polyline instance 
    var polyline = new fabric.Polyline([ 
      { x: 200, 
        y: 10 }, 
      {x: 250, 
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
        y: 10 }], { 
        stroke: 'green',  
        strokeWidth: 3,  
        cornerStyle: 'circle',  
        left: 100
      }); 

    // Render the polyline in canvas 
    canvas.add(polyline); 
  </script> 
</body> 

</html>
```

**输出:**

![](img/0c8801824754c8fd1d590cb9783bfea8.png)