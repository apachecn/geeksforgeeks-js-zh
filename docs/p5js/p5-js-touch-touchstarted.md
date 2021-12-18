# P5 . js Touch | Touch started()

> 原文:[https://www.geeksforgeeks.org/p5-js-touch-touchstarted/](https://www.geeksforgeeks.org/p5-js-touch-touchstarted/)

p5.js 中的 **touchStarted()** 函数在每次注册触摸后调用一次。如果未定义 **touchStarted()** 函数，则如果定义了 **mousePressed()** 函数，则将调用该函数。

**语法:**

```
touchStarted([Event])

```

下面的程序说明了 p5.js 中的 touchStarted()函数:
**示例-1:**

```
let valueX;
let valueY;

function setup() {

    // Create Canvas of size 500*500
    createCanvas(500, 500);
}

function draw() {
    // set background color
    background(200);

    fill('green');

    // set text and text size
    textSize(25);

    text('Touch to change color', 30, 30);

    // fill color according to touchStarted() 
    fill(valueX, 255 - valueY, 255 - valueX);

    // draw ellipse  
    ellipse(mouseX, mouseY, 115, 115);

}

function touchStarted() {
    valueX = mouseX % 255;
    valueY = mouseY % 255;
}
```

**输出:**
![](img/fc5a68a25d9120ef612833438988c1ff.png)

**示例-2:**

```
let valueX;
let valueY;

function setup() {
    // Create Canvas of size 500*500
    createCanvas(500, 500);
}

function draw() {
    // set background color
    background(200);
    fill('green');
    // set text and text size
    textSize(25);
    text('Touch to change color', 30, 30);
    // fill color according to mouseMoved() 
    fill(valueX, 255 - valueY, 255 - valueX);
    // draw rectangle 
    rect(mouseX, mouseY, 115, 115);
    fill(valueY, 255 - valueX, 255 - valueX);

    rect(mouseX, mouseY + 115, 115, 115);
    fill(255 - valueY, 255 - valueX, 255 - valueY);

    rect(mouseX - 115, mouseY, 115, 115);
    fill(255 - valueY, 255 - valueY, 255 - valueY);

    rect(mouseX - 115, mouseY + 115, 115, 115);

}

function touchStarted() {
    valueX = mouseX % 255;
    valueY = mouseY % 255;
}
```

**输出:**
![](img/885c4328e243f7946c2666d02e5f9e6b.png)

**参考:**T2】https://p5js.org/reference/#/p5/touchStarted