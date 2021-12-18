# p5.js | noStroke()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-nostroke-function/](https://www.geeksforgeeks.org/p5-js-nostroke-function/)

noStroke()函数是 p5.js 中的一个内置函数，用于移除用于在形状周围绘制线条和边框的轮廓。默认情况下，黑色描边设置为形状。

**语法:**

```
noStroke()
```

**参数:**该功能不接受任何参数。

下面的程序说明了 P5.js 中的 noStroke()函数:
**程序:**

```
function setup() {

    // Canvas size 400*400
    createCanvas(400, 400); 
}

function draw() {

    // Shape defined just below, will not have any outline
    noStroke(); 

    // Fill light-green color to shape
    fill('lightgreen'); 
    rect(20, 20, 160, 160);
}
```

**输出:**
![](img/e1e0c3bd77c9bc3058cb9bbac4a02581.png)

**参考:**T2】https://p5js.org/reference/#/p5/noStroke