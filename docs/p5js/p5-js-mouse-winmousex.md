# p5.js | Mouse | winmouseX

> 原文:[https://www.geeksforgeeks.org/p5-js-mouse-winmousex/](https://www.geeksforgeeks.org/p5-js-mouse-winmousex/)

p5.js 中的 **winmouseX** 变量用于存储鼠标相对于窗口(0，0)的当前水平位置。

**语法:**

```
mouseX
```

下面的程序说明了 p5.js 中的 mouseX 变量:

**示例 1:** 本示例使用 winmouseX 变量显示其位置。

```
function setup() {

    // Create canvas of given size
    createCanvas(1000, 400);

    // Set the text size
    textSize(20); 
}

function draw() {

    // Set the background color
    background(200);

    // Create rectangle
    rect(winMouseX, winMouseY, 10, 10);

    // Display position of winmouseX
    text("Position of winmouseX is " 
        + winMouseX, 30, 40);
}
```

**输出:**
![](img/dc518da7404ec191d6c25c05c42106a6.png)

**示例 2:** 本示例使用 winmouseX 变量，在满足条件的情况下显示一些内容。

```
function setup() {

    // Create canvas of given size 
    createCanvas(500, 500);

    // Set the text size
    textSize(20); 
}

function draw() {

    // Set the background color
    background(200);

    // Create circle
    circle(winMouseX, winMouseY, winMouseX-winMouseY);

    // Create line
    line(0, 0, windowWidth, windowHeight);

    // Check condition and execute statement
    if(winMouseX!=winMouseY ) {
        text("You Lose", 12, 34);
    }
}
```

**输出:**
![](img/2c5463f7a8adcaf0931f30b45dbfb911.png)

**参考:**T2】https://p5js.org/reference/#/p5/dwinmouseX