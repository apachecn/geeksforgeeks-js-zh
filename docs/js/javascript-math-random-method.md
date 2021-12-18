# JavaScript 数学随机()方法

> 原文:[https://www . geesforgeks . org/JavaScript-math-random-method/](https://www.geeksforgeeks.org/javascript-math-random-method/)

下面是数学随机()方法的例子。

*   **示例:**用于获取 0(包含)和 1(不包含)之间的随机数。

    ```
    <script type="text/javascript">
        var random = Math.random( );
        document.write("Random Number Generated : " + random ); 
    </script>
    ```

*   **输出:**

    ```
    Random Number Generated : 0.2894437916976895
    ```

**Math.random()** 函数用于返回一个介于[0，1]，0(包含)和 1(不包含)之间的浮点伪随机数。然后，可以根据所需的范围对该随机数进行缩放。

**语法:**

```
Math.random();
```

**参数**:本功能不接受任何参数。

**返回值:**math . random()函数返回一个介于[0，1]，0(包括 0)和 1(不包括 0)之间的浮点伪随机数。

以上方法的更多代码如下:
**程序 1:** Math.random()可以用来获取两个值之间的随机数。返回值不小于 min，可能等于 min，也可能小于不等于 max。要获得两个值之间的随机数，可以通过以下方式执行 math.random()函数:

```
<script type="text/javascript">
    var min=4;
    var max=5; 
    var random = Math.random() * (+max - +min) + +min;
    document.write("Random Number Generated : " + random ); 
</script>
```

**输出:**

```
Random Number Generated : 4.991720937372939
```

**程序 2:** Math.random()可以用来获取两个值之间的整数。返回值不小于最小值，或者如果最小值不是整数，则为下一个大于最小值的整数。也小于但不等于 max。要获得两个值之间的随机整数，可以通过以下方式执行 Math.random()函数:

```
<script type="text/javascript">
    var min=4;
    var max=5; 
    var random =
    Math.floor(Math.random() * (+max - +min)) + +min;
    document.write("Random Number Generated : " + random ); 
</script>                    
```

**输出:**

```
Random Number Generated : 4
```

**程序 3:** Math.random()可以用来获取最小值和最大值之间的整数，不仅包括最小值，还包括最大值。要获得两个值之间的随机整数，可以通过以下方式执行 Math.random()函数:

```
<script type="text/javascript">
    var min=20;
    var max=60; 
    var random =
    Math.floor(Math.random() * (+max + 1 - +min)) + +min;
    document.write("Random Number Generated : " + random ); 
</script>                    
```

**输出:**

```
Random Number Generated : 60
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队