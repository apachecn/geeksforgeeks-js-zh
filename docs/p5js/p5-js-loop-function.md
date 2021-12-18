# p5.js | loop()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-loop-function/](https://www.geeksforgeeks.org/p5-js-loop-function/)

**循环()函数**用于连续调用 draw()函数。可以使用 noLoop()函数停止 loop()函数。

**语法:**

```
loop()
```

下面的例子说明了 p5.js 中的**循环()**函数:

**示例:**

```
let l = 0;

function setup() {

  // Create canvas of given size
  createCanvas(500, 300);

  // Set the background color
  background('green');

}

function draw() {

  // Set the stroke color
  stroke('white');

  l = l + 0.5;
  if (l > width) {
    l = 0;
  }

  // Function to draw the line
  line(l, 0, l, height);

}

function mousePressed() {
  noLoop();
}

function mouseReleased() {
  loop();
}
```

**输出:**
![](img/9f454bad4dfc432c06f37b2fe0158871.png)

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)