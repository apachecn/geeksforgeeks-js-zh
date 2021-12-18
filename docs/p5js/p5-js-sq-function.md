# p5.js | sq()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-sq-function/](https://www.geeksforgeeks.org/p5-js-sq-function/)

p5.js 中的 **sq()** 函数用于*计算一个数*的平方值。数字的平方总是正数。

**语法**

```
sq(number)

```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **number:** This parameter stores the number to compute.

    下面的程序说明了 p5.js 中的 **sq()** 功能:
    T3】示例:

    ```
    function setup() {
        //create Canvas of size 270*80  
        createCanvas(270, 80);
    }

    function draw() {
        background(220);
        //initialize the parameter  
        let x = 4;
        //call to sq() function
        let y = sq(x);
        textSize(16);
        fill(color('red'));
        text("Given Number is : " + x, 50, 30);
        text("Computed Number is : " + y, 50, 50);
    }
    ```

    **输出:**
    ![](img/e6b0a6ed84819df88e8fd6afafad4c67.png)

    **参考:**T2】https://p5js.org/reference/#/p5/sq