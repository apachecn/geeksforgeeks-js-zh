# p5.js | filter()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-filter-function/](https://www.geeksforgeeks.org/p5-js-filter-function/)

**滤镜()**功能用于对画布应用滤镜。p5.js 有几个预设，可以用不同的强度级别来获得想要的效果。
**语法:**

```
filter( filterType, filterParam)
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **过滤器类型:**定义用作过滤器的预设的常数。它可以具有以下值:
    *   **阈值:**该模式用于根据可选级别参数中定义的阈值将图像转换为黑白。级别值为 0.0 意味着图像将是完全黑色的，值为 1.0 意味着图像将是白色的。如果未指定值，则使用 0.5。
    *   **灰度:**该模式将图像中的所有颜色转换为灰度等效色。可选参数不用于此预设。
    *   **不透明:**该模式将图像的 alpha 通道设置为完全不透明。可选参数不用于此预设。
    *   **反转:**该模式反转图像中的每个像素。可选参数不用于此预设。
    *   **POSTERIZE:** 该模式将图像的每个通道限制在值中指定的颜色数量内。可选参数可以设置在 2 到 255 的范围内，在较低的颜色范围内效果最明显。
    *   **模糊:**该模式对图像应用高斯模糊。可选参数用于指定模糊的强度。如果没有指定参数，则应用半径为 1 米的高斯模糊。
    *   **侵蚀:**该模式减少光照面积。可选参数不用于此预设。
    *   **扩张:**此模式增加光照面积。可选参数不用于此预设。
*   **过滤器参数:**是每个过滤器独有的数字，影响过滤器的功能。这是一个可选参数。

以下示例说明了 p5.js:
**示例 1:**
中的**过滤器()功能**

## java 描述语言

```
function preload() {
  img = loadImage("sample-image.png");
}

function setup() {
  filterModes = [
    GRAY,
    OPAQUE,
    INVERT,
    POSTERIZE,
    BLUR,
    ERODE,
    DILATE,
    BLUR,
    THRESHOLD
  ];

  index = 0;
  currFilterMode = filterModes[index];

  createCanvas(500, 300);
  textSize(20);

  btn = createButton("Change filter");
  btn.position(30, 200);
  btn.mousePressed(changeFilter);
}

function draw() {
  clear();

  text('Click on the button to change the filter mode', 20, 20);
  text("Current filter: " + currFilterMode, 20, 50);

  image(img, 20, 80);

  // Set the filter
  filter(currFilterMode);
}

function changeFilter() {
  if (index < filterModes.length - 1)
    index++;
  else
    index = 0;
  currFilterMode = filterModes[index];

  console.log("Current filter: " + currFilterMode);
}
```