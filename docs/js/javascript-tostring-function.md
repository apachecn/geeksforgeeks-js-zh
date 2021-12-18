# JavaScript Number toString()方法

> 原文:[https://www.geeksforgeeks.org/javascript-tostring-function/](https://www.geeksforgeeks.org/javascript-tostring-function/)

下面是 Number toString()方法的示例。

*   **例:**

    ```
    <script type="text/javascript">
        var num=12;
        document.write("Output : " + num.toString(2));          
    </script>
    ```

*   Output:

    ```
    Output:1100
    ```

Javascript 中的 **toString()** 方法用于数字，并将数字转换为字符串。它用于返回表示指定的 Number 对象的字符串。

**语法:**

```
*num*.toString(base)
```

toString()方法与数字 *num* 一起使用，如上面使用“.”的语法所示操作员。此方法会将 *num* 转换为字符串。

**使用的参数:**该方法接受单个可选参数**基础**。此参数指定字符串中表示整数的基数。它是一个介于 2 和 36 之间的整数，用于指定表示数值的基数。

**返回值:**num . tostring()方法返回一个表示指定数字对象的字符串。

下面是一些例子来说明 toString()方法在 JavaScript 中的工作方式:

1.  **将数字转换为基数为 2 的字符串**:要将数字转换为基数为 2 的字符串，我们必须通过传递 2 作为参数来调用 toString()方法。

    ```
    <script type="text/javascript">
        var num=213;
        document.write("Output : " + num.toString(2));          
    </script>
    ```

    输出:

    ```
    Output:11010101
    ```

2.  **将数字转换为以 8 为基数的字符串**:要将数字转换为以 8 为基数的字符串，我们必须通过传递 8 作为参数来调用 toString()方法。

    ```
    <script type="text/javascript">
        var num=213;
        document.write("Output : " + num.toString(8));          
    </script>
    ```

    输出:

    ```
    Output : 325
    ```

3.  **将数字转换为以 16 为基数的字符串**:要将数字转换为以 16 为基数的字符串，我们必须通过传递 16 作为参数来调用 toString()方法。

    ```

    <script type="text/javascript">
        var num=213;
        document.write("Output : " + num.toString(16));          
    </script>
    ```

    输出:

    ```
    Output : d5
    ```

4.  **当没有传递参数时**:如果在没有传递任何参数的情况下调用了 toString()方法，那么数字将被转换为字符串，而 BASE 中没有变化。下面是程序对此进行说明:

    ```
    <script type="text/javascript">
        var num=213;
        document.write("Output : " + num.toString());          
    </script>
    ```

    输出:

    ```
    Output :213
    ```

**支持的浏览器:**

*   谷歌铬
*   Internet browser
*   red fox
*   苹果旅行队
*   歌剧

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。