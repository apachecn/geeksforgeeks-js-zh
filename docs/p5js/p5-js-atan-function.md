# p5.js | atan()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-atan-function/](https://www.geeksforgeeks.org/p5-js-atan-function/)

p5.js 中的 **atan()函数**是*用来计算范围在**-无穷大**到**无穷大**(不含)之间的值的 **tan()** 或**反正切**的倒数，并给出范围在 **-π/2** 到 **π/2*** 的结果。

**语法:**

```
atan(P)
```

**参数:**该函数接受一个参数“P”，该参数是一个范围从-1 到 1 的值，其反正切被计算。

**返回值:**返回一个值的反正切，范围在-π/2 到π/2 之间。

下面的程序说明了 p5.js 中的 atan()函数:

**示例:**本示例使用 atan()函数来**获取一个值的反正切**。

```
function setup() { 

    // Create Canvas of size 270*80 
    createCanvas(550, 130); 
} 

function draw() { 

    // Set the background color 
    background(220); 

    // Initialize the parameter with some values
    let a = 0; 
    let b = 88; 
        let c = -1;
        let d = -0.5;
        let e = 5;

    // Call to atan() function 
    let v = atan(a);
        let w = atan(b);
        let x = atan(c);
        let y = atan(d);
        let z = atan(e);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting arc tangent value 
    text("Arc tangent value of 0 is : " + v, 50, 30);
        text("Arc tangent value of 88 is : " + w, 50, 50);
        text("Arc tangent value of -1 is : " + x, 50, 70);
        text("Arc tangent value of -0.5 is : " + y, 50, 90);
        text("Arc tangent value of 5 is : " + z, 50, 110);     
} 
```

**输出:**
![](img/5d882766e33116f6f0430a77454b33ca.png)

**参考:**T2】https://p5js.org/reference/#/p5/atan