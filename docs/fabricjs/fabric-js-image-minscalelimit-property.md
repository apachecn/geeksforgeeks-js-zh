# fabric . js Image minscalellimit 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-image-minscalelimit-property/](https://www.geeksforgeeks.org/fabric-js-image-minscalelimit-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布图像的最小比例限制，以便图像的大小不能缩小到该限制之外。画布图像意味着图像是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、形状、填充颜色或笔画宽度时，可以自定义图像。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含图像的主体标签中创建一个画布块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Image 的实例，并使用 minScaleLimit 属性设置 Image 的最小比例限制，并在 Canvas 上渲染 Image，如下例所示。

**语法**:

```html
fabric.Image(image, {
       minScaleLimit : number
});
```

**参数**:该功能取一个参数，如上所述，如下所述。

*   **最小刻度极限**:该参数取一个指定最小刻度极限的数值。

**示例**:本示例使用 Fabric.js 设置画布图像的 **minScaleLimit** 属性，如下例所示。

## 超文本标记语言

```html
<!DOCTYPE html> 
<html> 

<head> 
    <!-- Adding the FabricJS library -->
    <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
    </script> 
</head> 

<body> 
    <h1 style="color: green;"> 
        GeeksforGeeks 
    </h1> 

    <b> 
        Fabric.js | Image minScaleLimit Property 
    </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src= 
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"> 
    <br> 

    <script> 

        // Creating the instance of canvas object 
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image 
        var img = document.getElementById('my-image'); 

        // Creating the image instance 
        var geeks = new fabric.Image(img, {
            minScaleLimit : 1.2 
        }); 

        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/9f19ccfbf1405854c381e8bae5cc7bdb.png)