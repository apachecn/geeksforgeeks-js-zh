# p5.js | pow()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-pow-function/](https://www.geeksforgeeks.org/p5-js-pow-function/)

p5.js 中的**幂()函数**用于计算一个数对给定数的幂。这是一种将数字本身(或它们的倒数)大量相乘的有效方法。

**语法**

```
pow( n, e )

```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **n:** 此参数存储指数表达式的基数。*   **e:** This parameter stores the power by which to raise the base.

    下面的程序说明了 p5.js 中的 pow()函数:

    **示例:**本示例使用 power()函数计算一个数的幂。

    ```
    function setup() {

        // Create Canvas of size 270*80  
        createCanvas(350, 80);
    }

    function draw() {

        // Set the background color
        background(220);

        // Initialize the parameter  
        let n = 3;
        let e = 4;

        // Call to pow() function
        let y = pow(n, e);

        // Set the size of text
        textSize(16);

        // Set the text color
        fill(color('red'));

        text("Given number is " + n + " and exponent is " 
                +  e + " ", 50, 30);
        text("Computed Number is : " + y, 50, 50);
    }
    ```

    **输出:**
    ![](img/617074bb82be462f1214e08de00b0f75.png)

    **参考:**T2】https://p5js.org/reference/#/p5/pow