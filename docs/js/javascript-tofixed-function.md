# JavaScript Number toFixed()方法

> 原文:[https://www.geeksforgeeks.org/javascript-tofixed-function/](https://www.geeksforgeeks.org/javascript-tofixed-function/)

下面是 Number toFixed()方法的示例。

*   **例:**

    ```
    <script type="text/javascript">
        var test=213.73145;
        document.write(test.toFixed(1));          
    </script>
    ```

*   **输出:**

    ```
    213.7
    ```

JavaScript 中的 toFixed()方法用于使用定点表示法格式化数字。它可以用来格式化小数点右边有特定位数的数字。

**语法:**

```
*number*.toFixed( value )
```

toFixed()方法与一个*数字*一起使用，如上面使用“.”的语法所示操作员。此方法将使用定点表示法格式化数字。

**参数**:该方法接受单个参数**值**。它表示小数点后出现的位数。

**返回值:**返回字符串形式的数字。该数字在小数点后有精确的位数，如 toFixed()方法中所述。

**例**

*   **Using toFixed() method without any parameter**: If there is no parameter specified in the toFixed() method then it doesn’t display any digits after the decimal place.

    ```
    <script type="text/javascript">
        var test=213.73145;
        document.write(test.toFixed());          
    </script>
    ```

    **输出:**

    ```
    214
    ```

*   **Using toFixed() method with a parameter**: If there is a parameter specified in the toFixed() method will return a number represented as string which will have exactly that number of digits after the decimal place.

    ```
    <script type="text/javascript">
        var test=213.73145;
        document.write(test.toFixed(3));          
    </script>
    ```

    **输出:**

    ```
    214.731
    ```

*   **Using toFixed() method where the number is in exponential form**: The toFixed() method can be used to convert an exponential number into a string representation with a specific number of digits after the decimal place.

    ```
    <script type="text/javascript">
        var test=2.13e+15;
        document.write(test.toFixed(2));          
    </script>
    ```

    **输出:**

    ```
    2130000000000000.00
    ```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   苹果 Safari
*   歌剧