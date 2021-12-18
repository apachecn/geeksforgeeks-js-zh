# JavaScript 数学天花板( )方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-ceil-method/](https://www.geeksforgeeks.org/javascript-math-ceil-method/)

下面是**数学上限()**方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
             document.write("Result : " + Math.ceil(.89));
    </script>
    ```

*   **输出:**

    ```
    Result : 1
    ```

**数学天花板**方法用于返回大于或等于给定数字的最小整数。天花板()总是被用作数学天花板()，因为它是数学的静态方法。

**语法:**

```
Math.ceil(value)
```

**参数:**该方法接受上述和下述单个参数:

*   **值:**是要进行数学测试的值。

**返回值:**math . ceil()方法返回大于或等于给定数字的最小整数。

下面的例子说明了 JavaScript 中的数学天花板()方法:

*   **例 1:**

    ```
    Input : Math.ceil(.89)
    Output: 1
    ```

    *   **例 2:**

    ```
    Input :  Math.ceil(-89.02)
    Output : -89
    ```

    *   **Example 3:**

    ```
    Input : Math.ceil(0)
    Output : 0
    ```

    上述方法的更多代码如下:

    **程序 1:** 当负数作为参数传递时。

    ```
    <script type="text/javascript">
             document.write("Result : " + Math.ceil(-89.02));
    </script>
    ```

    **输出:**

    ```
    Result : -89
    ```

    **程序 2:** 当零作为参数传递时。

    ```
    <script type="text/javascript">
             document.write("Result : " + Math.ceil(0));
    </script>
    ```

    **输出:**

    ```
    Result : 0
    ```

    **支持的浏览器:**

    *   谷歌 Chrome
    *   微软公司出品的 web 浏览器
    *   火狐浏览器
    *   歌剧
    *   旅行队