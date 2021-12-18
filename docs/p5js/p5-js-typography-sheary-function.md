# p5.js |排版| shearY()功能

> 原文:[https://www . geesforgeks . org/P5-js-排版-sheary-function/](https://www.geeksforgeeks.org/p5-js-typography-sheary-function/)

p5.js 中的**sheray()函数**用于围绕 y 轴剪切形状或对象。对象被剪切了角度参数指定的量。为了使角度正常工作，应在当前角度模式下进行指定。对象总是围绕其相对于原点的位置沿顺时针方向剪切。

**语法:**

```
shearY(angle)
```

**参数:**该功能接受单参数**角度**，存储角度值。

下面的程序说明了 p5.js 中的 shearY()函数:

**示例 1:** 本示例使用 sheray()函数围绕 y 轴剪切对象。

```
function setup() {

    // Create Canvas of given size
    createCanvas(780, 650);
}

function draw() {

    // Set the background color
    background(220);

    // Set fill color
    fill('lightgreen');

    // Set stroke width
    strokeWeight(5);

    // Set shearY function
    shearY(PI/6);

    // Finally Draw the sheared rectangle
    rect(30, 30, 400, 300);
}
```

**输出:**
![](img/475b02dfb371579c2aeef4d916ceff77.png)

**示例 2:** 本示例使用 sheray()函数围绕 y 轴剪切对象。

```
function setup() {

    // Create Canvas of given size
    createCanvas(780, 650);
}

function draw() {

    // Set the background color
    background(220);

    // Set fill color
    fill('lightgreen');

    // Set stroke width
    strokeWeight(5);

    // Set shearY function
    shearY(PI/9);

    // Finally Draw the sheared
    // circle of radius 80 
    circle(height/2, width/2, 80);
}
```

**输出:**
![](img/ef96e340e94505f5e87995aecf9c6408.png)

**参考:**T2】https://p5js.org/reference/#/p5/shearY