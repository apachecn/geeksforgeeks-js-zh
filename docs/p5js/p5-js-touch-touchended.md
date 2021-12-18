# p5.js Touch | touchEnded()

> 原文:[https://www.geeksforgeeks.org/p5-js-touch-touchended/](https://www.geeksforgeeks.org/p5-js-touch-touchended/)

当触摸结束时，会调用 p5.js 中的 **touchEnded()** 函数。如果没有定义 **touchEnded()** 函数，如果定义了 **mouseReleased()** 函数，将会调用该函数。

**语法:**

```
touchEnded([Event])

```

下面的程序说明了 p5.js 中的 touchEnded()函数:
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
    // fill color according to touchEnded() 
    fill(valueX, 255 - valueY, 255 - valueX);
    // draw ellipse  
    ellipse(mouseX, mouseY, 115, 115);

}

function touchEnded() {
    valueX = mouseX % 255;
    valueY = mouseY % 255;
}
```

**输出:**
![](img/e79181c1c6020f0b5f0333be70f706db.png)

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

    text('Touch and Move to change color', 30, 30);
    // fill color according to touchEnded() 

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

function touchEnded() {
    valueX = mouseX % 255;
    valueY = mouseY % 255;
}
```

**输出:**
![](img/5efcc412d29ef32203c169a72c6593e0.png)
**参考:**[https://p5js.org/reference/#/p5/touchEnded](https://p5js.org/reference/#/p5/touchEnded)