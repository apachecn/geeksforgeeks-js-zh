# JavaScript 数学回合( )方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-round-method/](https://www.geeksforgeeks.org/javascript-math-round-method/)

下面是**数学轮()**方法的例子。

*   **示例:**将一个数字四舍五入到最接近的整数。

    ```
    <script type="text/javascript">
        var round =Math.round(5.8);
        document.write("Number after rounding : " + round); 
    </script>
    ```

*   **输出:**

    ```
    Number after rounding : 6
    ```

**Math.round()** 方法用于将一个数字舍入到最接近的整数。如果数字的小数部分大于或等于. 5，参数将舍入到下一个更高的整数。如果数字的小数部分小于. 5，参数将被舍入到下一个较低的整数。

**语法:**

```
Math.round(value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**是你要四舍五入的数字。

**返回值:**math . round()方法返回舍入到最接近整数的给定数字的值。

上述方法的更多代码如下:

**程序 1:** 当作为参数传递给 Math.round()方法时，该方法本身会舍入一个负数。要将负数舍入到其最接近的整数，应该以下列方式实现 Math.round()方法:

```
<script type="text/javascript">
    var round =Math.round(-5.8);
    document.write("Number after rounding : " + round); 
</script>
```

**输出:**

```
Number after rounding : -6
```

**程序 2:** 下面的程序显示了当参数有小数点“. 5”时，Math.round()方法的结果。

```
<script type="text/javascript">
    var round =Math.round(-12.5);
    document.write("Number after rounding : " + round +
    "<br>");
    var round =Math.round(12.51);
    document.write("Number after rounding : " + round); 
</script>
```

**输出:**

```
Number after rounding : -12
Number after rounding : 13
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队