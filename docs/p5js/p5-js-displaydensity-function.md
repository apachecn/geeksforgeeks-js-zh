# p5.js | displayDensity()函数

> 原文:[https://www . geesforgeks . org/P5-js-display density-function/](https://www.geeksforgeeks.org/p5-js-displaydensity-function/)

p5.js 中的 displayDensity()函数用于返回草图当前显示的像素密度。

**语法:**

```
pixelDensity(density)
```

**参数:**该功能接受存储显示密度的单参数**密度**。

下面的程序说明了 p5.js 中的 displayDensity()函数:

**示例:**

```
function setup() {

    // Create canvas of given size
    createCanvas(windowWidth, windowHeight);

    // Call the displayDensity function
    let density = displayDensity(); 
    pixelDensity(density);
}

function draw() {

    // Set the background color
    background(0, 200, 0);

    // Set text color
    color("green");

    // Set font size
    textSize(30);

    // Set text alignment
    textAlign(CENTER);

    // Set text to be add
    text("GeeksForGeeks!", windowWidth/2, windowHeight/2);

    // Display pixelDensity on the screen
    text("PixelDensity is " + pixelDensity(), 
            windowWidth/2, windowHeight/2+40);
}
```

**输出:**
![](img/82b41199acdeab6a460ec026633f578f.png)

**参考:**T2】https://p5js.org/reference/#/p5/displayDensity