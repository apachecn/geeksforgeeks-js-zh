# 织物线具有控制属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-has controls-property/](https://www.geeksforgeeks.org/fabric-js-line-hascontrols-property/)

在本文中，我们将在 **FabricJS** 中查看画布线中的角是否可见。帆布线是指线是可移动的，可以根据需要拉伸。此外，线条在初始*笔画颜色、高度、宽度、填充颜色、*或*笔画宽度时可以自定义。*

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化由 **FabricJS** 提供的画布和线条的实例。如果角是可见的，则由决定 ***控制*** 线的属性，并在画布上渲染线，如下所示。

**语法:**

```html
fabric.line({
    hasControls : boolean
});
```

**参数:**该属性接受一个参数，如上所述，如下所述。

*   **有控制:**指定是否能看到拐角。它包含一个布尔值。

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
   <h1>fabric.js | line hasControls  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>       

      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         hasControls: true

      }); 

      canvas.add(line); 

   </script> 
</body> 

</html> 
```

**输出:**

![](img/4c01e0ab6b491a5bf6ea0279546dd668.png)

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
   <h1>fabric.js | line hasControls  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>      

      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         hasControls: false

      }); 

      canvas.add(line); 

   </script> 
</body> 

</html> 
```

**输出:**

![](img/b4789861a9b2308dedfc71a63bcaba38.png)