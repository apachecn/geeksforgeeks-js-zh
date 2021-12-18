# JavaScript 数学 abs()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-abs-method/](https://www.geeksforgeeks.org/javascript-math-abs-method/)

下面是**数学 abs()** 方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
        document.write(Math.abs(-2)+"<br>"); 
        document.write(Math.abs(-2.56));          
    </script>
    ```

*   **输出:**

    ```
    2
    2.56
    ```

**Math.abs()** 方法用于返回一个数的绝对值。它以一个数字为参数，并返回其绝对值。

**语法:**

```
Math.abs(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**要找到绝对值的数字作为参数传递给该函数。

**返回:**作为参数传递的数字的绝对值。

以下示例说明了 JavaScript 中的 Math abs()方法:

*   **例 1:**

    ```
    Input  : Math.abs(-4)
    Output : 4
    ```

*   **例 2:**

    ```
    Input : Math.abs(0)
    Output : 0
    ```

**错误和异常:**

*   作为参数传递的非数字字符串返回 **NaN** 。
*   作为参数传递的超过 1 个整数的**数组返回 **NaN** 。**
*   作为参数传递的一个**空变量**返回 **NaN** 。
*   作为参数传递的**空字符串**返回 0。
*   作为参数传递的**空数组**返回 0。

上述方法的更多示例代码如下:

**程序 1:**

```
<!-- POSITIVE NUMBER EXAMPLE -->
<script type="text/javascript">
    document.write(Math.abs(2)+"<br>"); 
    document.write(Math.abs(2.56));          
</script>
```

**输出:**

```
2
2.56

```

**程序 2:**

```
<!-- STRING EXAMPLE -->
<script type="text/javascript">
    document.write(Math.abs("Geeksforgeeks"));          
</script>
```

**输出:**

```
NaN

```

**程序 3:**

```
<!-- ADDITION INSIDE FUNCTION EXAMPLE -->
<script type="text/javascript">
    document.write(Math.abs(7+9));           
</script>
```

**输出:**

```
16

```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队