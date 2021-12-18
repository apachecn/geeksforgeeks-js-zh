# JavaScript 数学 cos()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-cos-method/](https://www.geeksforgeeks.org/javascript-math-cos-method/)

下面是**数学 cos()** 方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
             document.write("The cos of 0 : " + Math.cos(0));
    </script>
    ```

*   **输出:**

    ```
    The cos of 0 : 1
    ```

**Math.cos()** 方法用于返回一个数的余弦值。Math.cos()方法返回一个介于-1 和 1 之间的数值，它代表以弧度表示的给定角度的余弦值。cos()是 Math 的静态方法，因此，它总是用作 Math.cos()，而不是创建的 Math 对象的方法。

**语法:**

```
Math.cos(value)
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **值:**此参数是以弧度给出的数字。

**返回:****数学 cos()** 函数返回给定数字的余弦值，范围从-1 到 1。

下面的例子说明了 JavaScript 中的 cos()方法:

*   **例 1:**

    ```
    Input: Math.cos(010)
    Output : -0.14550003380861354
    ```

*   **例 2:**

    ```
    Input: Math.cos(10)
    Output : -0.8390715290764524
    ```

以上方法的更多代码如下:
**程序 1:** 当 1 作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.cos(1));
</script>
```

**输出:**

```
Result : 0.5403023058681398
```

**程序 2:** 当 PI 作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.cos(Math.PI));
</script>
```

**输出:**

```
Result : -1
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队