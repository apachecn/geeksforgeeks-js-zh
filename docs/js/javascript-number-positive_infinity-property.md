# JavaScript Number 正数 _INFINITY 属性

> 原文:[https://www . geesforgeks . org/JavaScript-number-正数 _infinity-property/](https://www.geeksforgeeks.org/javascript-number-positive_infinity-property/)

下面是 Number 正数 _INFINITY 属性的示例。

*   **例:**

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;
    document.write(a * 10);
    </script>
    ```

*   **输出:**

    ```
    Infinity
    ```

在 javascript 中**数字。正无穷大**代表最大正值，即正无穷大。数字的实际值。正值无限与全局对象的**无限**属性的值相同。

**语法:**
可以用下面的方法给变量赋值。

```
var a = Number.POSITIVE_INFINITY
```

现在，我们知道什么是**数了。POSITIVE_INFINITY** ，我们来看一些例子，看看对 Number 进行的一些算术运算的结果。正数 _ 无穷大。

*   **Example 1:** When we multiply any positive number including **Number.POSITIVE_INFINITY** by **Number.POSITIVE_INFINITY** the result is **Number.POSITIVE_INFINITY**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;

    document.write(a * 2);
    </script>
    ```

    **输出:**

    ```
    Infinity
    ```

*   **Example 2:** When we multiply any negative number with **Number.POSITIVE_INFINITY** the result is **negative Infinity**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;
    document.write(a * -2);
    <script>
    ```

    **输出:**

    ```
    Infinity
    ```

*   **Example 3:** When we divide any positive or negative number by **Number.POSITIVE_INFINITY** the result is **0**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;

    document.write(2 / a);
    </script>
    ```

    **输出:**

    ```
    0
    ```

*   **Example 4:** When we multiply **Number.POSITIVE_INFINITY** by **0**, result is **NaN**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;

    document.write(a * 0);
    </script>
    ```

    **输出:**

    ```
    NaN
    ```

*   **Example 5:** When we divide **Number.POSITIVE_INFINITY** by any **negative** number except **Number.NEGATIVE_INFINITY**, result is **Number.NEGATIVE_INFINITY.**

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;

    document.write(a / -2);
    </script>
    ```

    **输出:**

    ```
    Infinity
    ```

*   **Example 6:** When we divide **Number.POSITIVE_INFINITY** by any **positive** number except **Number.POSITIVE_INFINITY**, result is **Number.POSITIVE_INFINITY**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;

    document.write(a / 2);
    </script>
    ```

    **输出:**

    ```
    Infinity
    ```

*   **Example 7:** When we divide **Number.POSITIVE_INFINITY** by either **NEGATIVE_INFINITY** or **POSITIVE_INFINITY**, result is **NaN**.

    ```
    <script>
    var a = Number.POSITIVE_INFINITY;
    var b = Number.NEGATIVE_INFINITY;

    document.write(a / b);
    </script>
    ```

    **输出:**

    ```
    NaN
    ```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   苹果 Safari
*   歌剧