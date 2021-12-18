# 如何在 webGL 和 p5.js 中创建三维几何图形？

> 原文:[https://www . geeksforgeeks . org/如何创建三维几何图形-in-webgl-and-p5-js/](https://www.geeksforgeeks.org/how-to-create-3d-geometries-in-webgl-and-p5-js/)

在本文中，我们将看到如何在 p5.js 中绘制 3D 几何图形(包含长度、宽度和高度)。p5.js 中的默认渲染用于 2D 图像，对于 3D 图像，我们使用 **WEBGL** ，它通过在几何图形中引入 Z 维度来启用 3D 渲染。

**语法:**

```
createCanvas( windowWidth, windowHeight, WEBGL )
```

**示例 1:** 在本例中，我们将使用 webGL 和 p5.js 创建一个 3D 几何图形，并向各个方向旋转。

## Javascript

```
// Create a canvas of given size
let angle = 0;

function setup() {
    createCanvas(600, 600, WEBGL);
}

// Create a draw function
function draw() {
    background(175);
    ambientLight(255);
    push();

    // Rotate the box in all dimensions
    translate(mouseX - width / 2,
            mouseY - width / 2);

    rotateX(angle);
    rotateZ(angle * 0.03);
    rotateY(angle * 0.06);
    noStroke();
    normalMaterial();

    // Create box of given size
    box(150, 150, 150);
    push();
    angle += .06
}
```