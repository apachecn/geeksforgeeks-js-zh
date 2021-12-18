# 织物. js 图像角点阵列属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-cornerdasharray-property/](https://www.geeksforgeeks.org/fabric-js-image-cornerdasharray-property/)

**Fabric.js** 是一个用来处理画布的 javascript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。图像的 cornerDashArray 属性用于设置画布图像的控制角的虚线图案。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS，并使用图像对象的 cornerDashArray 属性设置控制画布图像的角的虚线模式。

**语法:**

```
fabric.Image(image, {
    cornerDashArray:[Number]
});
```

**参数:**该函数取两个参数，如上所述，描述如下:

*   **图像:**该参数取图像。
*   **角点阵列:**此参数定义画布图像控制角点的虚线图案。

**示例:**本示例使用 FabricJS 将虚线图案设置为画布图像的控制角，如下例所示。

```

<!DOCTYPE html> 
<html> 

<head> 
    <!-- Adding the FabricJS library -->
    <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
    </script> 
</head> 

<body> 
    <h1 style="color: green;">GeeksforGeeks</h1> 
    <b>Fabric.js | Image cornerDashArray Property </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"><br>

    <script> 
        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 
        var img= document.getElementById('my-image');
        var imgInstance = new fabric.Image(img, {
            cornerColor:"red",
            cornerDashArray:[5]
        });
        canvas.add(imgInstance);
    </script> 
</body> 

</html>
```

**输出:**

![](img/3b956b34a8d91d5edbf8a2c802941fbb.png)