# JavaScript 数学 SQRT2 属性

> 原文:[https://www . geesforgeks . org/JavaScript-math-sqrt2-property/](https://www.geeksforgeeks.org/javascript-math-sqrt2-property/)

下面是**数学 SQRT2** 属性的例子。

*   **例:**

    ```
    <script>
      // Here value of Math.SQRT2 is printed.
      document.write(Math.SQRT2);
    </script>
    ```

*   **输出:**

    ```
    1.4142135623730951
    ```

数学。SQRT2 是 JavaScript 中的一个属性，简单来说就是用来求 2 的平方根值，其值近似为 **1.4142** 。
就是说，

> √t0〖2〗t1〖1.4142

**语法:**

```
Math.SQRT2;
```

**返回值:**它只是返回 2 的平方根值，其值约为 1.4142。

下面的例子说明了 JavaScript 中的数学 SQRT2 属性。

*   **Example:** Here the simple value of the square root of 2 is shown as output.

    ```
    Input : Math.SQRT2
    Output : 1.4142135623730951
    ```

    以上属性的更多代码如下:
    **程序 1:**2 的平方根值可以如下所示的函数形式打印。

    ```
    <script>
      // function is being called.
      function get_Value_of_square_root()
      {
          return Math.SQRT2;
      }

      // function is calling for getting
      // value of square root of 2
      document.write(get_Value_of_square_root());
    </script>
    ```

    **输出:**

    ```
    1.4142135623730951
    ```

    **程序 2:** 这里我们考虑数学。SQRT2 作为一个函数，但实际上它是一个属性，这就是为什么错误作为输出被显示。

    ```
    <script>
      // Here we consider Math.SQRT2 as a function 
      // but in actual it is a property that is why error
      // as output is being shown.
      document.write(Math.SQRT2(12));
    </script>
    ```

    **输出:**

    ```
    Error: Math.SQRT2 is not a function
    ```

    **程序 3:** 它的应用是求 2 的平方根值，这是借助这个性质来完成的。在数学上，它需要很多。
    T3】例:

    ```
    <script>
      // Value of Math.SQRT2 is printed.
      document.write(Math.SQRT2);
    </script>
    ```

    **输出:**

    ```
    1.4142135623730951
    ```

    **支持的浏览器:**

    *   谷歌 Chrome
    *   微软公司出品的 web 浏览器
    *   火狐浏览器
    *   歌剧
    *   旅行队