# Fabric.js 路径锁频属性

> 原文:[https://www . geesforgeks . org/fabric-js-path-lockscalingx-property/](https://www.geeksforgeeks.org/fabric-js-path-lockscalingx-property/)

在本文中，我们将看到如何使用 **Fabric.js** 设置路径的 **lockScalingX** 。Fabric.js 中的路径是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义路径。

为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含路径的画布块。之后，我们将初始化由 **Fabric.js** 和提供的画布和路径的实例，使用 **lockScalingX** 属性锁定画布路径在 x 方向上的缩放。

**语法:**

```
fabric.Path('path', {
  lockScalingX: Boolean
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **lockScalingX:** 指定画布的缩放是否水平锁定。

下面的例子说明了在 JavaScript 中使用 fabric . js**Path lockScalingX**属性:

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
      Fabric.js | Path lockScalingX Property 
    </b> 
  </div> 

  <div style="text-align: center;"> 
    <canvas id="canvas" width="400" height="200"
      style="border:1px solid green;"> 
    </canvas> 
  </div> 

  <script> 
    // Initiate a Canvas instance 
    var canvas = new fabric.Canvas("canvas"); 

    var geek = new fabric.Path(
    'M 0 0 L 100 100 L 0 100 z', {
      fill: 'green',
      lockScalingX: true
    });

    canvas.add(geek);
    canvas.centerObject(geek);
  </script> 
</body> 

</html>
```

**输出:**

![](img/242edad941db78dc18aa211b11ed914e.png)