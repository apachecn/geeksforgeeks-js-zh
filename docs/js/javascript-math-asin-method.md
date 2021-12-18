# JavaScript 数学 asin()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-asin-method/](https://www.geeksforgeeks.org/javascript-math-asin-method/)

下面是**数学 asin( )** 方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
       document.write("When 1 is  passed as a parameter: " 
                     + Math.asin(1));
    </script>
    ```

*   **输出:**

    ```
    When 1 is  passed as a parameter: 1.5707963267948966
    ```

**Math.asin( )** 方法用于返回以弧度为单位的数字的反正弦。Math.asin()方法返回一个介于-pi/2 和 pi/2 弧度之间的数值。asin()是 Math 的静态方法，因此，它总是用作 Math.asin()，而不是创建的 Math 对象的方法。

> math . asin(x)= arcsin(x)=唯一 y
> 其中 y 属于[-pi/2；π/2]
> 使得 sin(y)=x

**语法:**

```
Math.asin(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**这个参数保存一个弧度数，你要找谁的反正弦。

**返回:**方法返回给定弧度数的反正弦值。

下面的例子说明了 JavaScript 中的数学 asin()方法:

*   **例 1:**

    ```
    Input : Math.asin(1)
    Output : 1.5707963267948966
    ```

*   **例 2:**

    ```
    Input : Math.asin(-1)
    Output : -1.5707963267948966
    ```

*   **例 3:**

    ```
    Input : Math.asin(2)
    Output : NaN
    ```

*   **例 4:**

    ```
    Input : Math.asin(0.5)
    Output : 0.5235987755982989
    ```

上述方法的更多示例代码如下:

**程序 1:**

```
<script type="text/javascript">
    document.write("When -1 is  passed as a parameter: " 
                   + Math.asin(-1));
</script>
```

**输出:**

```
When -1 is  passed as a parameter: -1.5707963267948966
```

**程序 2:**

```
<script type="text/javascript">
    document.write("When 2 is  passed as a parameter: " 
                   + Math.asin(2));
</script>
```

**输出:**

```
When 2 is  passed as a parameter: NaN
```

**程序 3:**

```
<script type="text/javascript">
    document.write("When 0.5 is  passed as a parameter: " 
                   + Math.asin(0.5));
</script>
```

**输出:**

```
When 0.5 is  passed as a parameter: 0.5235987755982989
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队