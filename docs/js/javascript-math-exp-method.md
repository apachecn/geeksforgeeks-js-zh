# JavaScript 数学 exp()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-exp-method/](https://www.geeksforgeeks.org/javascript-math-exp-method/)

下面是**数学 exp()** 方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
       document.write("When zero is  passed as a parameter: " 
             + Math.exp(0));
    </script>
    ```

*   **输出:**

    ```
    When zero is  passed as a parameter: 1
    ```

**Math.exp()** 方法用来返回 e <sup>x</sup> ，其中 x 是自变量，e 是欧拉数，欧拉数是自然对数的基数。exp()是 Math 的静态方法，因此，它总是用作 Math.exp()，而不是创建的 Math 对象的方法。

**语法:**

```
Math.exp(value)
```

**使用的参数:**该函数接受如上所述的单个参数，如下所述:

*   **值**是一个你想查找其 e <sup>x</sup> 的数字。

**返回:****数学表达式()**方法返回 e <sup>x</sup> ，其中 e 是欧拉数，x 是自变量。

以上方法的更多代码如下:
**程序 1:** 当“-1”作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.exp(-1));
</script>
```

**输出:**

```
Result : 0.36787944117144233 
```

**程序 2:** 当“1”作为参数传递时。

```
<script type="text/javascript">
         document.write("Result : " + Math.exp(1));
</script>
```

**输出:**

```
Result :  2.718281828459045 
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队