# fabric . js active selection lock movementx 属性

> 原文:[https://www . geesforgeks . org/fabric-js-activeselection-lock movementx-property/](https://www.geeksforgeeks.org/fabric-js-activeselection-lockmovementx-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布动态选举是用于创建动态选举实例的 fabric.js 类之一。画布活动选择意味着活动选择是可移动的，可以根据需要拉伸。在本文中，我们将使用 lockMovementX 属性来锁定水平移动。

首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含动态选择的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 ActiveSelection 类的实例。JS 并使用 lockMovementX 属性来锁定水平移动。

**语法:**

```html
fabric.ActiveSelection(ActiveSelection, {
    lockMovementX : boolean
});
```

**参数:**该属性采用如上所述的单个参数，描述如下:

*   **lockMovementX:** 此参数采用布尔值。它指定是否锁定画布的水平移动。

**示例:**本示例使用 FabricJS 设置画布 ActiveSelection 的 lockMovementX 属性，如下例所示。

## 超文本标记语言

```html
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
         Fabric.js | ActiveSelection lockMovementX Property 
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
        lockMovementX  : true
      });

      canvas.setActiveObject(gfg);
      canvas.requestRenderAll();
      canvas.centerObject(gfg); 
   </script> 
</body> 

</html>
```

**输出:**

![](img/8c5f6ff2a2dd05a480ef80f8f53729d2.png)