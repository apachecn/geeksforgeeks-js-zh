# p5.js |全屏()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-fullscreen-function/](https://www.geeksforgeeks.org/p5-js-fullscreen-function/)

p5.js 中的**全屏()功能**用于获取用户浏览器窗口的当前全屏状态。如果给定了一个参数，则根据该参数的值将草图设置为全屏或不全屏。如果没有给定参数，则返回当前全屏状态。请注意，由于浏览器的限制，这只能在用户输入时调用。

**语法:**

```
fullscreen()
```

**参数:**函数不接受任何参数。

下面的程序说明了 p5.js 中的全屏()函数:

**示例:**

```
function setup() {

    // Set the background color
    background(200);
}
function mousePressed() {

    // Set the value of fullscreen
    // into the variable
    let fs = fullscreen();

    // Call to fullscreen function
    fullscreen(!fs); 
}
```

**输出:**
**点击屏幕前:**
![](img/a3662574e80f00a430de1735d4fa48f0.png)

**点击屏幕后:**
![](img/b75b80208e5ff175cf2a3514abdf4ba3.png)

**参考:**T2】https://p5js.org/reference/#/p5/fullscreen