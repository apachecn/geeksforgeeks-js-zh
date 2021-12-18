# JavaScript 数学 min()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-min-method/](https://www.geeksforgeeks.org/javascript-math-min-method/)

下面是数学最小值()方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
         document.write("When  positive numbers are passed"+
                        " as parameters: " + Math.min(10, 32, 2));
    </script>
    ```

*   **输出:**

    ```
    When  positive numbers are passed as parameters: 2
    ```

**Math.min()** 方法用于返回方法中传递的最低值数字。如果任何参数不是数字并且不能转换为数字，则 Math.min()方法返回 NaN。min()是 Math 的静态方法，因此，它总是用作 Math.min()，而不是创建的 Math 对象的方法。

**语法:**

```
Math.min(value1, value2, ...)
```

**参数:**该方法接受可使用 n 次的单个参数，如上所述，如下所述:

*   **值:**该值发送给 **math.min()** 方法求最大值。

**返回值:****math . min()**方法返回给定数字中的最小值。

以下示例说明了 JavaScript 中的数学最小值()方法:

*   **例 1:**

    ```
    Input : Math.min(10, 32, 2)
    Output: 2
    ```

*   **例 2:**

    ```
    Input : Math.min(-10, -32, -1)
    Output: -32
    ```

*   **例 3:**

    ```
    Input : Math.min()
    Output: Infinity
    ```

*   **例 4:**

    ```
    Input : Math.min(10,2,NaN)
    Output: Nan
    ```

上述方法的更多代码如下:

以上方法的更多代码如下:
**程序 1:** 当负数作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.min(-10, -32, -1));
</script>
```

**输出:**

```
Result : -32
```

**程序 2:** 无参数通过时。

```
<script type="text/javascript">
         document.write("Result : " + Math.min());
</script>
```

**输出:**

```
Result : Infinity
```

**程序:**当 NaN 作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.min(10,2,NaN));
</script>
```

**输出:**

```
Result : NaN
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队