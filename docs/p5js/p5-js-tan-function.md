# p5.js | tan()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-tan-function/](https://www.geeksforgeeks.org/p5-js-tan-function/)

p5.js 中的 **tan()函数**用于计算作为函数输入参数的弧度角的正切值。

**语法:**

```
tan(angle)
```

**参数:**该函数接受单个参数**角度**，这是一个弧度角度，其正切值将被计算。

**返回值:**返回以弧度为单位的角度的正切值作为输入参数。

下面的程序说明了 p5.js 中的 tan()函数:

**示例:**本示例使用 tan()函数获取一个角度在弧度上的正切值。

```
function setup() { 

    // Create Canvas of given size 
    createCanvas(550, 130); 
} 

function draw() { 

    // Set the background color 
    background(220); 

    // Initialize the parameter with
    // angles in radian only
    let a = 0; 
    let b = 8.9; 
    let c = 47;
    let d = 5;

    // Call to tan() function 
    let v = tan(a);
    let w = tan(b);
    let x = tan(c);
    let y = tan(d);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting tangent value 
    text("Tangent value of angle 0 (in radian) is : " + v, 50, 30);
    text("Tangent value of angle 8.9 (in radian) is : " + w, 50, 50);
    text("Tangent value of angle 47 (in radian) is : " + x, 50, 70);
    text("Tangent value of angle 5 (in radian) is : " + y, 50, 90);     
} 
```

**输出:**
![](img/2ef540ff680fd59deb369b2b3d385f10.png)

**注意:**在上面的代码中，输入角度应以弧度为单位。要将度数转换为弧度，请使用以下公式:

```
Angles_in_radian = (π/180)*angles_in_degree
```

**参考:**T2】https://p5js.org/reference/#/p5/tan