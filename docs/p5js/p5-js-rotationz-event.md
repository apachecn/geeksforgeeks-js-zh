# p5.js 旋转 z 事件

> 原文:[https://www.geeksforgeeks.org/p5-js-rotationz-event/](https://www.geeksforgeeks.org/p5-js-rotationz-event/)

p5.js 中的系统变量 **rotationZ** 负责移动设备(智能手机和平板电脑)始终沿着 z 轴的旋转。它可以在 draw()函数中使用，以连续获取当前沿 z 轴的旋转。如果图形角度模式()设置为度数，则该值将在 0 到 360 的范围内。当设置为 RADIANS 时，该值将为 0 到 2*PI。该变量仅适用于内置指南针的设备。

**注意:**如果三个变量一起使用，旋转的调用顺序很重要。需要按照 Z、Y 和 X 的顺序调用它们，以防止不一致。

**语法:**

```
rotationZ
```

**例 1:**

## java 描述语言

```
// Rotate the the device to see the box move
function setup() {
  createCanvas(600, 600, WEBGL);
}

function draw() {
  background(2);

  // Set the rotation to be equal to
  // the variable rotationZ
  rotateZ(radians(rotationZ));

  fill("blue");
  box(200, 200, 200);
}
```

**输出:**

![](img/7a14b7f6088e103cba552d0751908ae2.png)

**例 2:**

## java 描述语言

```
function setup() {
  createCanvas(600, 600, WEBGL);
}

function draw() {
  background(205, 105, 94);

  // Set the rotation to be equal to
  // the variable rotationZ
  rotateZ(radians(rotationZ));

  fill('green');
  cylinder(100, 200);
}
```

**输出:**

![](img/b686c08ce36d6c49338a1ba9f4d5250f.png)