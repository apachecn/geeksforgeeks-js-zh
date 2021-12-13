# 织物线透明角属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-transparentcorners-property/](https://www.geeksforgeeks.org/fabric-js-line-transparentcorners-property/)

在本文中，我们将使用 **【透明角落】**属性来在 **FabricJS** 中设置画布线条中角落的透明度。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

**语法:**

```html
fabric.line({
  ransparentCorners: boolean
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化 **FabricJS** 和提供的画布和线条的实例，使用 **transparentCorners** 属性设置画布线条中角落的透明度，并在画布上渲染线条，如下所示。**

**参数:**该属性具有如上所述的单一值，如下所述:

*   **透明角落:**指定画布线中角落的透明度。包含布尔值。

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
   <h1>fabric.js | line transparentCorners property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas");
      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         transparentCorners : true
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html>
```

**输出:**

![](img/b00ea2f5e2c5f8e2beb2fba6b74fcf73.png)

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
   <h1>fabric.js | line transparentCorners property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 
      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         transparentCorners : false
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html>
```

**输出:**

![](img/4ee18e38fa1b67f488d6d7d63a33ad77.png)