# p5.js 预加载()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-preload-function/](https://www.geeksforgeeks.org/p5-js-preload-function/)

p5.js 中的**预加载()函数**用于在 setup()函数之前异步加载文件。加载草图时，它只运行一次。

大多数用户不使用 preload()函数，因为在 setup()函数中可以完成相同的任务。然而，在我们的程序中分离类似的代码来提高它的可伸缩性和模块化是很好的。一般 preload()函数是用来加载像图像、3D 模型、字体等东西的。在草图里。在加载资源的过程中会显示“加载...”文本。

**语法:**

```
preload() {
   // All loading calls here
}
```

**参数:**此功能不接受任何参数。

下面的例子说明了 p5.js 中的**预加载()功能**:

**例 1:**

## java 描述语言

```
let gfg_img;
function preload() {

  // Loading the image
  gfg_img = loadImage('/gfg.png');
}

function setup() {
  createCanvas(400, 400);
}

function draw() {

  // Set background color to green
  background('green');

  // Show loaded image on screen at (100, 100)
  image(gfg_img, 100, 100);
}
```

**输出:**

![](img/f716a3fba245395509f2465325efebdb.png)

**例 2:**

## java 描述语言

```
let cylinder;
function preload() {

  // Loading a cylinder model
  cylinder = loadModel('/cylinder.stl', true);
}

function setup() {
  createCanvas(400, 400, WEBGL);
  noLoop();
}

function draw() {

  // Set background color to green
  background('green');

  // Display and rotate the model
  rotateX(90);
  model(cylinder);
}
```

**输出:**

![](img/3df95e0f068b06c9abff0e4735f6bb32.png)