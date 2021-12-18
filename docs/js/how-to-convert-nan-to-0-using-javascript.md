# 如何用 JavaScript 将 NaN 转换为 0？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 将 nan 转换为 0/](https://www.geeksforgeeks.org/how-to-convert-nan-to-0-using-javascript/)

NaN(不是数字)通常用于指示函数的错误情况，该函数应该返回一个有效的数字，但是可以使用 JavaScript 将其转换为 0。在本文中，我们将把 NaN 转换为 0。

**使用 isNan()方法:**使用 isNaN()方法检查给定的编号是否为 NaN。如果 isNaN()为“number”返回 true，那么它将赋值 0。

*   **例:**

    ```
    <script>
        number = NaN;
        if (isNaN(number)) number = 0;
        console.log(number);
    </script>
    ```

*   **Output:**

    ```
    0
    ```

**使用||运算符:**如果“数字”是任何假值，它将被指定为 0。

*   **例:**

    ```
    <script>
        number = NaN;
        number = number || 0;
        console.log(number);
    </script>
    ```

*   **Output:**

    ```
    0
    ```

**使用三进制运算符:**这里的数字是通过三进制运算符来检查的，类似于 1，如果 NaN 转换为 0。

*   **例:**

    ```
    <script>
        number = NaN;
        number = number ? number : 0;
        console.log(number);
    </script>
    ```

*   **Output:**

    ```
    0
    ```

**注意:**在我们的 IDE 或您的浏览器上执行代码时，检查控制台(F12)查看结果。