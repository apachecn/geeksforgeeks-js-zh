# JavaScript 数学 atan()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-atan-method/](https://www.geeksforgeeks.org/javascript-math-atan-method/)

下面是**数学 atan( )** 方法的例子。

*   **例:**

    ```
    <script type="text/javascript">
         document.write("When 1 is  passed as a parameter: " 
         + Math.atan(1));
    </script>
    ```

*   **输出:**

    ```
    When 1 is  passed as a parameter: 0.7853981633974483
    ```

**Math.atan( )** 方法用于以弧度为单位返回数字的反正切。Math.atan()方法返回一个介于-pi/2 和 pi/2 弧度之间的数值。atan()是 Math 的静态方法，因此，它总是用作 Math.atan()，而不是创建的 Math 对象的方法。

> math . atan(x)= arctan(x)=唯一 y
> 其中 y 属于[-pi/2；π/2]
> 使得 tan(y)=x

**语法:**

```
Math.atan(value)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **x:** 这是一个以弧度为单位的数字，你想找谁的反正切。

**返回:**函数的作用是:以弧度为单位返回给定数字的反正切值。

下面的例子说明了 JavaScript 中的 Math atan()方法

*   **例 1:**

    ```
    Input : Math.atan(1)
    Output : 0.7853981633974483
    ```

*   **例 2:**

    ```
    Input : Math.atan(0)
    Output : 0
    ```

*   **例 3:**

    ```
    Input : Math.atan(-0)
    Output : -0
    ```

*   **例 4:**

    ```
    Input : Math.atan(Infinity)
    Output :  1.5707963267948966
    ```

*   **例 5:**

    ```
    Input : Math.atan(-Infinity)
    Output :  -1.5707963267948966
    ```

上述方法的更多示例代码如下:

**程序 1:**

```
<script type="text/javascript">
      document.write("When 0 is  passed as a parameter: " 
      + Math.atan(0));
</script>
```

**输出:**

```
When 0 is  passed as a parameter: 0
```

**程序 2:**

```
<script type="text/javascript">
    document.write("When -0 is  passed as a parameter: " 
                   + Math.atan(-0));
</script>
```

**输出:**

```
When -0 is  passed as a parameter: 0
```

**程序 3:**

```
<script type="text/javascript">
         document.write("When Infinity is  passed as a parameter: " 
                        + Math.atan(Infinity));
</script>
```

**输出:**

```
When Infinity is  passed as a parameter: 1.5707963267948966
```

**程序 4:**

```
<script type="text/javascript">
         document.write("When -Infinity is  passed as a parameter: " 
         + Math.atan(-Infinity));
</script>
```

**输出:**

```
When -Infinity is  passed as a parameter: -1.5707963267948966
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队