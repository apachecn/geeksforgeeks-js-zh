# p5.js | rotateX()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-rotatex-function/](https://www.geeksforgeeks.org/p5-js-rotatex-function/)

p5.js 中的 **rotateX()函数**用于围绕 x 轴旋转形状或对象。
**语法:**

```
rotateX(angle)
```

**参数:**该功能接受单个参数**角度**，该参数存储旋转角度。
下面的程序说明了 p5.js:
**中的 rotateX()函数示例 1:** 本示例使用 rotateX()函数围绕 x 轴旋转对象。

## java 描述语言

```
function setup() {

    // Create Canvas of given size
    createCanvas(800, 550, WEBGL);
}

function draw() {

    // Set the background color
    background(220);

    // Set stroke weight
    strokeWeight(12);

    // Rotation function
    rotate(PI / 7.0);

    // Call to rotateX function
    rotateX(millis() / 1000);

    // Draw rectangle
    rect(3, 3, 200, 39);

    // Draw ellipse
    ellipse(160, 160, 40, 40);
}
```

**输出:**

![](img/619fee9b05742f7ddedbd5ea99da0dc5.png)

**示例 2:** 本示例使用 rotateX()函数围绕 x 轴旋转对象。

## java 描述语言

```
function setup() {

    // Create canvas of given size
    createCanvas(500, 500, WEBGL);
}

function draw() {

    // Set background color
    background(200);

    // Set property to rotate the
    // shape about the x-axis
    rotateX(frameCount * 0.01);

    // Set stroke weight
    strokeWeight(2);

    // Set fill color
    fill("green");

    // Draw of height 100 and radius 50
    cylinder(50, 100);
}
```

**输出:**

![](img/3cc040a503a38829edc3b38bcbc9f49d.png)

**参考:**T2https://p5js.org/reference/#/p5/rotateX