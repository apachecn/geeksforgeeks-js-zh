# p5.js | createSlider()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-createslider-function/](https://www.geeksforgeeks.org/p5-js-createslider-function/)

p5.js 中的 createSlider()函数用于在 DOM(文档对象模型)中创建一个滑块(输入)元素。这个函数包括 p5.dom 库。在标题部分添加以下语法。

```
<script src=
"https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.11/addons/p5.dom.min.js">
</script>
```

**语法:**

```
createSlider( min, max, value, step )
```

**参数:**该功能接受四个参数，如上所述，描述如下:

*   **min:** 保持滑块的最小值。
*   **最大:**它保存滑块的最大值。
*   **值:**保存滑块的默认值。
*   **步长:**它保存滑块的步长。

下面的程序说明了 p5.js 中的 createSlider()函数:

**示例:**本示例使用 createSlider()函数，使用滑块更改背景色(rgb 格式)的 *r* 值。

```
// Create a variable for the slider object
var color_slider;

function setup() {

    // Create a canvas of given size
    createCanvas(600, 300);

    // Create the slider
    color_slider = createSlider(0, 255, 125);

    // Set the position of slider on the canvas
    color_slider.position(150, 200);
}

function draw() {

    // Get the value of the slider
    // using .value() function
    col = color_slider.value();

    // Set the value of the background-color
    background(col, 200, 100);
}                    
```

**输出:**
![](img/5013b946d2d16747a48b94d156336db5.png)

**参考:**T2】https://p5js.org/reference/#/p5/createSlider