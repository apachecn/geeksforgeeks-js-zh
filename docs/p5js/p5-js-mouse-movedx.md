# p5.js |鼠标移动

> 原文:[https://www.geeksforgeeks.org/p5-js-mouse-movedx/](https://www.geeksforgeeks.org/p5-js-mouse-movedx/)

p5.js 中的 **movedX** 变量包含从草图的最后一帧开始鼠标的水平移动。正值表示鼠标向右移动，负值表示鼠标在最后一帧向左移动。

**语法:**

```
movedX

```

下面的程序说明了 p5.js 中的 **movedX** 变量:
**示例 1:**

## java 描述语言

```
function setup() {
  createCanvas(400, 300);
  textSize(16);

  fpsSlider = createSlider(1, 60, 30, 1);
  fpsSlider.position(20, 40);
}

function draw() {
  clear();
  text("Move the slider to change the framerate "+
       "of the sketch", 20, 20);

  // Set the framerate according to the slider
  frameRate(fpsSlider.value());
  text("Current Framerate: " + fpsSlider.value() + " FPS", 20, 80);

  // Use the movedX property
  text("The mouse moved " + movedX + " units in the x-direction", 20, 140);
  text("since the last frame", 20, 160);
}
```