# fabric . js active selection lock movementy Property

> 原文:[https://www . geesforgeks . org/fabric-js-activeselection-lock movementy-property/](https://www.geeksforgeeks.org/fabric-js-activeselection-lockmovementy-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布动态选举是用于创建动态选举实例的 fabric.js 类之一。画布活动选择意味着活动选择是可移动的，可以根据需要拉伸。在本文中，我们将使用 lockMovementY 属性来锁定垂直移动。

首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含动态选择的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 ActiveSelection 类的实例。JS 并使用 lockMovementY 属性来锁定垂直移动。

**语法:**

```
fabric.ActiveSelection(ActiveSelection, {
lockMovementY : boolean
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **锁定移动:**它指定设置为真的选项是否会锁定垂直移动。它包含一个布尔值。

**示例:**本示例使用 FabricJS 设置画布 ActiveSelection 的 lockMovementY 属性，如下例所示。

**index.html**

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
         Fabric.js | ActiveSelection lockMovementY Property 
      </b> 

   </div> 

   <div style="text-align: center;"> 
      <canvas id="canvas" width="500" height="500"
            style="border:1px solid green;"> 
      </canvas> 
   </div> 
   <img src= 
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;">
   <script> 
      var canvas = new fabric.Canvas("canvas"); 

        // Initiate a Rect instance  
        var rectangle = new fabric.Rect({  
            width: 200,  
            height: 100,  
        });  
      canvas.add(rectangle); 

      var geek = new fabric.IText('GeeksforGeeks', {
      });
      canvas.add(geek);
      canvas.centerObject(geek); 

         var gfg = new fabric.ActiveSelection(canvas.getObjects(), {
            lockMovementY : true
         });
         canvas.setActiveObject(gfg);
         canvas.requestRenderAll();
         canvas.centerObject(gfg); 

   </script> 
</body> 

</html>
```

**输出:**

![](img/ae23948b0e055498402bb19a044934ab.png)