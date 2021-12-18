# p5.js |帧率()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-framerate-function/](https://www.geeksforgeeks.org/p5-js-framerate-function/)

p5.js 中的 frameRate()函数用于指定每秒显示的帧数。在没有参数的情况下调用 frameRate()将返回当前的帧率。draw 函数在返回值之前必须至少运行一次。该函数与 getFrameRate()函数相同。

**语法**

```
frameRate( c )
```

**参数:**该功能接受单参数 **c** ，存储帧率变量值。

下面的程序说明了 p5.js 中的 frameRate()函数:

**示例:**

```
function setup() {

    // Create canvas of given size
    createCanvas(500, 200);

    // Set the font size
    textSize(20);

    // Use frameRate() function
    frameRate(3);
}

function draw() {

    // Set the background color
    background(0, 153, 0);

    // Display the output
    text("Frame Count with frameRate " + 
         int(getFrameRate()), 100, 100);
}
```

**输出:**
![](img/bbfe494e09404676d41c578b1eb0e31c.png)

**参考:**T2】https://p5js.org/reference/#/p5/frameRate