# fabric . js line lockscaliflip 属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-lockscalingflip-property/](https://www.geeksforgeeks.org/fabric-js-line-lockscalingflip-property/)

在本文中，我们将查看设置为 *true 的选项*是否会在 **FabricJS** 中锁定画布线中的翻转。帆布线是可移动的，可以根据需要拉伸。此外，线条可以在初始*笔画颜色、高度、宽度、填充颜色、*或*笔画宽度方面进行自定义。*

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化由 **FabricJS** 和提供的画布和线条实例，看看设置为 *true* 的选项是否会使用**lockscaliflip**属性锁定画布线条在中的翻转，并在画布上渲染线条，如下所示。

**语法:**

```html
fabric.line({
    lockScalingFlip : boolean
});
```

**参数:**该属性接受一个参数，如上所述，如下所述。

*   **锁定锁定唇:**指定如果选项设置为*真*将锁定翻转。它包含一个布尔值。

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
   <h1>fabric.js | line lockScalingFlip property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>      

      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         lockScalingFlip : true

      }); 

      canvas.add(line); 

   </script> 
</body> 

</html> 
```

**输出:**

![](img/d97006f12715909ca888e00ee23feaa1.png)

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
   <h1>fabric.js | line lockScalingFlip property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>       

      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         lockScalingFlip  : false
      }); 

      canvas.add(line); 

   </script> 
</body> 

</html> 
```

**输出:**

![](img/73edbce6498e93974ff7153d4ad11214.png)