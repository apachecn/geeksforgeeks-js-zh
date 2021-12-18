# Fabric.js 线动画属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-flipy-property/](https://www.geeksforgeeks.org/fabric-js-line-flipy-property/)

在本文中，我们将看到如何在 **FabricJS** 中垂直翻转一条画布线。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

**语法:**

```
fabric.line({
    flipY : boolean
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化由 **FabricJS** 提供的画布和线的实例，并使用 **flipY** 属性垂直翻转画布线，并在画布上渲染线，如下所示。**

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **翻转:**指定如何垂直翻转对象。它包含一个布尔值。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
   <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
   </script> 
</head> 

<body> 
   <h1>fabric.js | line flipY  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         flipY: true
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/63bbd06f4b2249bf9d4d852ccdfe27f1.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
   <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
   </script> 
</head> 

<body> 
   <h1>fabric.js | line flipY  property</h1>

   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         flipY: false
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/9e7a5158d2e2cd4aa1bfdf416d54f664.png)