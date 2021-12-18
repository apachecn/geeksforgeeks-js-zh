# JavaScript 数学日志( )方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-log-method/](https://www.geeksforgeeks.org/javascript-math-log-method/)

下面是**数学日志()**方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
         document.write("When zero is  passed as a parameter: " 
                         + Math.log(0));
    </script>
    ```

*   **输出:**

    ```
    When zero is  passed as a parameter: -Infinity
    ```

用于返回数字的自然对数(以 e 为底)的 **Math.log()** 方法。JavaScript Math.log()方法相当于数学中的 ln(x)。如果 x 的值为负，则 math.log()方法返回 NaN。

log()是 Math 的静态方法，因此，它总是用作 Math.log()，而不是创建的 Math 对象的方法。

**语法:**

```
Math.log(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**这个参数保存一个你想求其自然对数的数字。

**返回值:**math . log()方法返回给定数字的自然对数。

上述方法的更多代码如下:

**程序 1:** 当“-1”作为参数传递时。

```
<script type="text/javascript">
         document.write("Result: " + Math.log(-1));
</script>
```

**输出:**

```
Output : NaN
```

**程序 12:** 当“10”作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.log(10));
</script>
```

**输出:**

```
Result : 2.302585092994046
```

**程序 3:** 用不同的基数计算数学对数()。要找到以 2 为底的 8 的对数，请按以下方式执行 math.log()方法:

```
<script type="text/javascript">
         document.write("Result : " + Math.log(8)/Math.log(2));
</script>
```

**输出:**

```
Output : 3
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队