# p5.js |三角形()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-triangle-function/](https://www.geeksforgeeks.org/p5-js-triangle-function/)

triangle()函数是 p5.js 中的一个内置函数，用于在平面上绘制三角形。这个函数接受三角形的三个顶点。
**语法:**

```
triangle(x1, y1, x2, y2, x3, y3)
```

**参数:**该功能接受六个参数，如上所述，描述如下:

*   **x1:** 该参数接受第一点的 x 坐标。
*   **y1:** 该参数接受第一点的 y 坐标。
*   **x2:** 该参数接受第二点的 x 坐标。
*   **y2:** 该参数接受第二点的 y 坐标。
*   **x3:** 该参数接受第三点的 x 坐标。
*   **y3:** 此参数接受第三点的 y 坐标。

下面的程序说明了 p5.js 中的三角()函数:

*   **节目 1:**

## java 描述语言

```
function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(220);
    fill('lightgreen');

    // A triangle at (100, 250), (250, 170) and (330, 300) 
    triangle(100, 250, 250, 170, 330, 300);
}
```