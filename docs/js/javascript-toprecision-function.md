# JavaScript Number toPrecision()方法

> 原文:[https://www . geesforgeks . org/JavaScript-to precision-function/](https://www.geeksforgeeks.org/javascript-toprecision-function/)

下面是 Number toPrecision()方法的示例。

*   **例:**

    ```

    <script type="text/javascript">
        var num=213.45689;
        document.write(num.toPrecision(3));          
    </script>
    ```

*   输出:

    ```
    213
    ```

Javascript 中的 **toPrecision()** 方法用于将数字格式化为特定的精度或长度。如果格式化的数字需要比原始数字更多的数字，则还会添加小数和空值来创建指定的长度。

**语法:**

```
*number*.toPrecision(value)
```

toPrecision()方法与一个*数字*一起使用，如上面使用“.”的语法所示操作员。此方法将数字格式化为指定的长度。

**参数:**该方法接受单个参数**值**。此参数也是可选的，它表示用户在格式化数字中想要的有效位数的值。

**返回值:**JavaScript 中的 toPrecision()方法返回一个字符串，该字符串中的数字被格式化为指定的精度。

下面是一些例子来说明 toPrecision()方法:

1.  **Passing no arguments in the toPrecision() method**: If no arguments is passed to the toPrecision() method then the formatted number will be exactly the same as input number. Though, it will be represented as a string rather than a number.
    **Code# 1:**

    ```

    <script type="text/javascript">
        var num=213.45689;
        document.write(num.toPrecision());          
    </script>
    ```

    输出:

    ```
    213.45689
    ```

2.  **Passing an argument in the toPrecision() method**: If the length of precision passed to the toPrecision() method is smaller than the original number then the number is rounded off to that precision.
    **Code# 2:**

    ```
    <script type="text/javascript">
        var num=213.45689;
        document.write(num.toPrecision(4));          
    </script>
    ```

    输出:

    ```
    213.5
    ```

3.  **Passing an argument which results in addition of null in the output**: If the length of precision passed to the toPrecision() method is greater than the original number then zero’s are appended to the input number to meet the specified precision.
    **Code# 3:**

    ```
    <script type="text/javascript">
        var num=213.45689;
        document.write(num.toPrecision(12));  

        var num2 = 123;
        document.write(num2.toPrecision(5));        
    </script>
    ```

    输出:

    ```
    213.456890000
    123.00

    ```

**注意:**如果指定的精度不在 1 到 100(包括 1 和 100)之间，将导致范围错误。

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   苹果 Safari
*   歌剧