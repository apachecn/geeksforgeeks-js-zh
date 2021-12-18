# JavaScript 数学 sin()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-sin-method/](https://www.geeksforgeeks.org/javascript-math-sin-method/)

下面是**数学罪恶()**方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
          document.write("When zero is  passed as a parameter: " 
                         + Math.sin(0));
    </script>
    ```

*   **输出:**

    ```
    When zero is  passed as a parameter: 0
    ```

Javascript 中的 **Math.sin()** 方法用于返回数字的正弦值。Math.sin()方法返回一个介于-1 和 1 之间的数值，它代表以弧度表示的给定角度的正弦值。

sin()是 Math 的静态方法，因此，它总是被用作 Math.sin()，而不是作为创建的 Math 对象的方法。

**语法:**

```
Math.sin(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:
**值**是以弧度给出的数字。

**返回值:**方法返回给定数字的正弦值。

下面的例子说明了 JavaScript 中的数学 sin()方法:

*   **例 1:**

    ```
    Input : Math.sin(0)
    Output : 0
    ```

*   **例 1:**

    ```
    Input : Math.sin(1)
    Output : 0.8414709848078965
    ```

*   **例 1:**

    ```
    Input : Math.sin(Math.PI / 2)
    Output : 1
    ```

以上方法的更多代码如下:
**程序 1:** 当 1 作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.sin(1));
</script>
```

**输出:**

```
Result : 0.8414709848078965
```

**程序 2:** 当 PI 作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.sin(Math.PI / 2));
</script>
```

**输出:**

```
Result : 1
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队