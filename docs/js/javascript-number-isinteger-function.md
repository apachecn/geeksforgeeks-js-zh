# JavaScript Number.isInteger()方法

> 原文:[https://www . geesforgeks . org/JavaScript-number-is integer-function/](https://www.geeksforgeeks.org/javascript-number-isinteger-function/)

下面是 Number.isInteger()方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
        document.write(Number.isInteger(-2)+"<br>");
        document.write(Number.isInteger(0)+"<br>"); 
        document.write(Number.isInteger(2));          
    </script>
    ```

*   输出:

    ```
    true
    true
    true
    ```

JavaScript 中的 Number.isInteger()方法用于检查传递给它的值是否为整数。如果传递的值是整数，则返回 true，否则返回 false。

**语法:**

```
Number.isInteger(value)
```

**参数:**该方法接受单个参数**值**，该值指定用户要检查整数的数字。

**返回值:**number . Isinteger()方法返回一个布尔值，即 true 或 false。如果传递的值是数字和整数类型，它将返回真，否则返回假。

以下示例说明了 JavaScript 中的 Number.isInteger()方法:

1.  **Passing a negative number as an argument**: If a negative integer value is passed to the method as an argument then the method will return true, if the negative value passed to it is not of integer type then the method will return false.

    ```
    <script type="text/javascript">
        document.write(Number.isInteger(-2)); 
        document.write(Number.isInteger(-2.56));          
    </script>
    ```

    输出:

    ```
    true
    false

    ```

2.  **Passing a positive number as an argument**: If a positive integer value is passed to the method as argument then the method will return true, if the positive value passed to it is not of integer type then the method will return false.

    ```
    <script type="text/javascript">
        document.write(Number.isInteger(2));          
    </script>
    ```

    输出:

    ```
    true
    ```

3.  **Passing a zero as an argument**: If zero is passed to the Number.isInteger() method then it will return true as zero is also an integer.

    ```
    <script type="text/javascript">
        document.write(Number.isInteger(0));          
    </script>
    ```

    输出:

    ```
    true
    ```

4.  **传递一个由小数位组成的数字作为参数**:如果一个小数位作为参数
    传递，该方法将返回 false。

    ```
    <script type="text/javascript">
        document.write(Number.isInteger(2.03));          
    </script>
    ```

    输出:

    ```
    false
    ```

5.  **将字符串作为参数传递**:如果传递给 Number.isInteger()方法的参数是字符串类型，那么它将返回 false。

    ```
    <script type="text/javascript">
        document.write("Output : " + Number.isInteger("hi"));          
    </script>
    ```

    输出:

    ```
    false
    ```

**支持的浏览器:**

*   谷歌 Chrome 19
*   Internet Explorer 12
*   Firefox 16
*   Apple Safari 09
*   歌剧 22

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。