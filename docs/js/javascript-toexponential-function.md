# JavaScript Number to exponential()方法

> 原文:[https://www . geesforgeks . org/JavaScript-to exponential-function/](https://www.geeksforgeeks.org/javascript-toexponential-function/)

下面是 Number toExponential()方法的示例。

*   **例:**

    ```

    <script type="text/javascript">
        var num = 212.13456;
        document.write(num.toExponential(4));          
    </script>
    ```

*   输出:

    ```
    Output :2.1213e+2
    ```

JavaScript 中的 toExponential()方法用于将数字转换为其指数形式。它返回一个以指数表示法表示 Number 对象的字符串。

**语法:**

```
*number*.toExponential(value)
```

toExponential()方法与数字一起使用，如上面使用“.”的语法所示操作员。这个方法将把一个数转换成它的指数形式。

**参数:**该方法接受单个参数*值*。它是一个可选参数，表示指定小数点后位数的值。

**返回值:**JavaScript 中的 toExponential()方法返回一个字符串，该字符串以指数形式表示给定的*数字*，小数点前有一位数字。

以下示例说明了在 JavaScript 中 toExponential()方法的工作原理:

1.  Passing a number as an argument in the toExponential() method. If a number is passed as an argument to the toExponential() method then it represents the number of digits after the decimal point.
    **Code# 1:**

    ```

    <script type="text/javascript">
        var num = 2.13456;
        document.write(num.toExponential(2));          
    </script>
    ```

    输出:

    ```
    2.13e+0
    ```

2.  Passing no parameter in the toExponential() method. Below program illustrates this:
    **Code# 2:**

    ```

    <script type="text/javascript">
        var num = 2.13456;
        document.write(num.toExponential());          
    </script>
    ```

    输出:

    ```
    2.13456e+0
    ```

3.  Passing a value which has more than 1 digit before the decimal point in the toExponential() method. Below program illustrates this:
    **Code# 3:**

    ```

    <script type="text/javascript">
        var num=212.13456;
        document.write(num.toExponential());          
    </script>
    ```

    输出:

    ```
    2.1213456e+2
    ```

4.  Passing zero as a parameter in the toExponential() method. Below program illustrates this:
    **Code# 4:**

    ```

    <script type="text/javascript">
        var num = 212.13456;
        document.write(num.toExponential(0));          
    </script>
    ```

    输出:

    ```
    Output :2e+2
    ```

**异常**:

1.  **范围错误**:当传递的*值*参数太小或太大时，抛出此异常。介于 0 和 20 之间的值(包括 0 和 20)不会导致范围错误。如果您想传递大于或小于此范围指定的值，则必须相应地实现 toExponential()方法。
2.  **类型错误**:当在非*号*类型的对象上调用 toFixed()方法时，会引发此异常。

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   苹果 Safari
*   歌剧