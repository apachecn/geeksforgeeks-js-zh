# p5.js |宽度变量

> 原文:[https://www.geeksforgeeks.org/p5-js-width-variable/](https://www.geeksforgeeks.org/p5-js-width-variable/)

p5.js 中的**宽度**变量是一个系统变量，*存储绘图画布*的宽度。一旦执行代码，该值将由 **createCanvas()** 函数的第一个参数自动初始化。

**语法:**

```
width

```

**参数:**此功能不接受任何参数。

下面的程序举例说明了 p5.js 中的宽度变量:
**例-1:**

```
function setup() {

    //create Canvas of size 380*80  
    createCanvas(380, 80);
}

function draw() {

    // set background color
    background(220);

    // set text size 
    textSize(16);

    // set the text alignment 
    textAlign(CENTER);

    //set the fill color
    fill(color('Green'));

    //use of width variable
    text("Width of Canvas is : "
         + width, 180, 50);
}
```

**输出:**
![](img/7b04bd5f038afd77c6367d09e11fbc7c.png)

**示例-2:**

```
function setup() {

    //create Canvas of size 380*80 
    width = windowWidth;
    createCanvas(width, 80);
}

function draw() {
    // set background color
    background(220);

    // set text size 
    textSize(16);

    // set the text alignment 
    textAlign(CENTER);

    //set the fill color
    fill(color('Green'));

    //use of width variable
    text("Width of Canvas is equal to windowWidth i.e. : "
         + width, 180, 50);
}
```

**输出:**
![](img/779a1644faf7fac08d0d759c3087fe3a.png)

**参考:**T2】https://p5js.org/reference/#/p5/width