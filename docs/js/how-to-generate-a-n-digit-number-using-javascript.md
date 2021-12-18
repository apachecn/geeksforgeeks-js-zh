# 如何用 JavaScript 生成一个 n 位数？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 生成一个 n 位数的数字/](https://www.geeksforgeeks.org/how-to-generate-a-n-digit-number-using-javascript/)

任务是在 JavaScript 的帮助下生成一个 n 位数的随机数。

下面讨论两种方法。在第一个例子中，它使用了这许多数字的最小和最大数量，而第二个例子使用了 **[子串](https://www.geeksforgeeks.org/javascript-string-substring/)** 的概念来修剪数字。
你也可以使用 JavaScript 生成给定范围内的随机数。

**方法 1:** 分别获取变量 min 和 max 中 n 位数的最小值和最大值。然后使用 **[Math.random()](https://www.geeksforgeeks.org/javascript-math-random-function/)** 生成一个随机数(值介于 0 和 1 之间)。将数字乘以**(最大-最小+1)** ，得到其楼层值，然后**将最小**值相加。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>
    <head>
        <title>
            Generate a n-digit number using JavaScript
        </title>
        <style>
            body {
                text-align: center;
            }
            h1 {
                color: green;
            }
            #geeks {
                color: green; 
                font-size: 29px;
                font-weight: bold;
            }
        </style>
    </head>

    <body>
        <h1>  
          GeeksforGeeks  
        </h1>
        <p>

          <!-- min and max are 5 digit so-->        
          Click on the button to generate random 
          5 digit number
        </p>
        <button onclick="gfg();">
            click here
        </button>
        <p id="geeks">
        </p>
        <script>
            var up = document.getElementById('GFG_UP');
            var down = document.getElementById('geeks');

            function gfg() {
                var minm = 10000;
                var maxm = 99999;
                down.innerHTML = Math.floor(Math
                .random() * (maxm - minm + 1)) + minm;
            }
        </script>
    </body>

    </html>
    ```

*   **输出:** ![](img/326c4f53549a8cd9ebb9470556a71887.png)

**方法二:**使用 **[Math.random()方法](https://www.geeksforgeeks.org/javascript-math-random-function/)** 生成一个 0 到 1 之间的随机数。现在我们将使用 **[。substring()方法](https://www.geeksforgeeks.org/javascript-string-substring/)** 把随机数转换成字符串后得到一部分。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Generate a n-digit number using JavaScript
        </title>
        <style>
            body {
                text-align: center;
            }
            h1 {
                color: green;
            }
            #geeks {
                color: green; 
                font-size: 29px;
                font-weight: bold;
            }
        </style>
    </head>

    <body style="text-align:center;">
        <h1 style="color:green;"> 
            GeeksforGeeks 
        </h1>
        <p>
            Click on the button to generate random 6 digit number
        </p>
        <button onclick="gfg();">
            click here
        </button>
        <p id="geeks">
        </p>
        <script>
            var down = document.getElementById('geeks');

            function gfg() {
                down.innerHTML = ("" + Math.random()).substring(2, 8);
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/fa1111910a4216512d4a7b22ed5e0887.png)