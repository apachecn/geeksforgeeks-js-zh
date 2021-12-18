# JavaScript 数学 trunc()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-trunc-method/](https://www.geeksforgeeks.org/javascript-math-trunc-method/)

下面是**数学 trunc()** 方法的例子。

*   **示例:**当一个正浮点数作为参数传递时

    ```
    <script type="text/javascript">
             document.write(Math.trunc(15.56));         
    </script>
    ```

*   **输出:**

    ```
    15
    ```

Math.trunc()方法用于通过移除小数来返回浮点数的整数部分。换句话说，Math.trunc()函数切断了点及其右边的数字。

**语法:**

```
Math.trunc(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值**。它是要发送给 Math.trunc()函数的浮点数。

**返回值:**方法返回给定数字的整数部分。

上述方法的更多代码如下:
**程序 1:** 当一个浮点数作为参数传递时

```
<script type="text/javascript">
         document.write(Math.trunc(-15.56));         
</script>
```

**输出:**

```
-15
```

**程序 2:** 当 0 到 1 之间的正数作为参数传递时:

```
<script type="text/javascript">
         document.write(Math.trunc(0.236));         
</script>
```

**输出:**

```
0
```

**程序 3:** 当 0 到 1 之间的负数作为参数传递时:

```
<script type="text/javascript">
         document.write(Math.trunc(-0.236));         
</script>
```

**输出:**

```
0
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队