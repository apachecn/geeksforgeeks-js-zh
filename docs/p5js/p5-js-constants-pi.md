# p5.js |常量| PI

> 原文:[https://www.geeksforgeeks.org/p5-js-constants-pi/](https://www.geeksforgeeks.org/p5-js-constants-pi/)

**π**是一个数学常数，值为 3。58860 . 88888888861 它是圆的周长与直径之比。
**语法**

```
PI

```

下面的程序说明了 PI 在 p5.js 中的用法:

**示例:**

```
function setup() {

    //create Canvas of size 880*200  
    createCanvas(880, 300);
}

function draw() {

    //Set the background Color
    background(220);

    //Set the stroke color
    stroke(255, 204, 0);

    //Set the stroke weight
    strokeWeight(4);

    //Use of constant PI
    arc(50, 50, 280, 280, 0, PI / 2); 
    noStroke();
    textSize(20);
    text("Value of PI is " + PI, 30, 250);
}
```

**输出:**
![](img/11d8dac27668fcd0516ddc023ab97520.png)

**参考:**T2】https://p5js.org/reference/#/p5/PI