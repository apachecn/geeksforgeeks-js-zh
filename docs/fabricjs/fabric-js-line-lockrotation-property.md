# 织物线锁定旋转属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-lock rotation-property/](https://www.geeksforgeeks.org/fabric-js-line-lockrotation-property/)

在本文中，我们将查看设置为 true 的选项是否会在 **FabricJS** 中锁定画布线中的旋转。帆布线是指线是可移动的，可以根据需要拉伸。 此外，线条可以自定义初始笔画颜色、高度、宽度、填充颜色或笔画宽度。

**语法:**

```
fabric.line({
    lockRotation : boolean
});
```

**方法:** 为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化 **FabricJS** 提供的画布和线条的实例，看看设置为 true 的选项是否会使用**锁定旋转** 属性锁定画布线条中的旋转，并在画布上渲染线条，如下所示。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **锁定旋转:**它指定如果选项设置为真将锁定旋转。它包含一个布尔值。

例 1:

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

   <h1>fabric.js | line lockRotation property</h1>

   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas>  

   <script> 
      // Initiate a Canvas instance 
      var canvas = new fabric.Canvas("canvas"); 
      // Initiate a Line instance 
      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         lockRotation : true
      }); 
      // Render the Line in canvas 
      canvas.add(line); 
   </script> 

</body> 

</html> 
```

**输出:**

![](img/18f4f2487ba6753f9acc22d07cc97d2e.png)

锁定旋转=真

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
   <h1>fabric.js | line lockRotation property</h1>

   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>         
      // Initiate a Canvas instance 
      var canvas = new fabric.Canvas("canvas"); 
      // Initiate a polyline instance 
      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         lockRotation : false
      }); 
      // Render the polyline in canvas 
      canvas.add(line); 
   </script> 

</body> 

</html> 
```

**输出:**

![](img/1d03866ab96b3d4c9bda78944c67c64f.png)

锁定旋转=假