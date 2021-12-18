# P5 . js | strokewight()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-strokeweight-function/](https://www.geeksforgeeks.org/p5-js-strokeweight-function/)

p5.js 中的**strokewight()函数**用于设置线条、点和形状周围边框的笔画宽度。笔画粗细通过使用像素来设置。

**语法:**

```
strokeWidth(weight)
```

**参数:**该功能接受单参数**权重**，存储笔画的权重(以像素为单位)。

下面的程序说明了 p5.js 中的 strokeWeight()函数:

**例 1:** 本例使用 strokeWeight()函数设置笔画宽度。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    // Set the background color
    background(220);

    // Set the stroke width
    strokeWeight(20);

    // Set the filled color
    fill('green');

    // Draw the circle
    circle(60, 60, 34);

    // Set the text size
    textSize(20);

    // Set the text to print
    text("GeeksForGeeks", 120, 70);
}
```

**输出:**
![](img/9d66ca5cdbcdd3962d9177f23e79acd9.png)

**例 2:** 本例使用 strokeWeight()函数设置笔画宽度。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    // Set the background color
    background(220);

    // Set the stroke clor
    stroke('orange');

    // Set the stroke width to 10
    strokeWeight(10); // Orange

    // Draw a line
    line(20, 70, 80, 70);

    // Set the stroke color
    stroke('white');

    // Set the stroke width to 8
    strokeWeight(8); // White

    // Draw a line
    line(20, 90, 80, 90);

    // Set stroke color
    stroke('green');

    // Set the stroke width to 6
    strokeWeight(6); // Green

    // Draw a line
    line(20, 110, 80, 110);
}
```

**输出:**
![](img/9dd72448c706fa300371594a9f568150.png)

**参考:**T2】https://p5js.org/reference/#/p5/strokeWeight