# p5.js | abs()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-abs-function/](https://www.geeksforgeeks.org/p5-js-abs-function/)

p5.js 中的 **abs()函数**用于*计算一个数字的绝对值*。这个函数映射到 javascript 的 **Math.abs()** 。一个数的绝对值总是正数。

**语法**

```
abs(number)

```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **number** : This parameter stores the number to compute.

    下面程序举例说明 **abs()函数**在 P5 . js:
    T3】示例:

    ```
    function setup() {
        //create Canvas of size 270*80  
        createCanvas(270, 80);
    }

    function draw() {
        background(220);
        //initialize the parameter  
        let x = -11;
        //call to abs() function  
        let y = abs(x);
        textSize(16);
        fill(color('red'));
        text("Given Number is : " + x, 50, 30);
        text("Computed Number is : " + y, 50, 50);

    }
    ```

    **输出:**
    ![](img/f3093097e8fd5dea994c4cb6e5a81ff0.png)

    **参考:**T2】https://p5js.org/reference/#/p5/abs