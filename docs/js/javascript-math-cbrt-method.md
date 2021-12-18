# JavaScript 数学 cbrt()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-cbrt-method/](https://www.geeksforgeeks.org/javascript-math-cbrt-method/)

下面是数学 cbrt()方法的例子。

*   **例:**

    ```
    <script type="text/javascript"> 
       document.write("cbrt of 64 : " 
                         + Math.cbrt(64) + "<br>");
       document.write("cbrt of 27: " 
                         + Math.cbrt(27) + "<br>"); 
       document.write("cbrt of 0: " 
                         + Math.cbrt(0) + "<br>"); 
       document.write("cbrt of -1: " 
                         + Math.cbrt(-1) + "<br>"); 
       document.write("cbrt of -27: " 
                         + Math.cbrt(-27) + "<br>"); 
       document.write("cbrt of Infinity : " 
                         + Math.cbrt(Infinity)); 
    </script> 
    ```

*   **输出:**

    ```
    cbrt of 16: 4
    cbrt of 27: 3
    cbrt of 0: 0
    cbrt of -1: -1
    cbrt of -27: -3
    cbrt of Infinity : Infinity
    ```

**Math.cbrt()** 方法用来求一个数的立方根。
**语法:**

```
Math.cbrt(x)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **x:** 这个参数只是一个需要求立方根的数字。

**返回:**返回给定数字的立方根。

下面的示例说明了 JavaScript 中的 cbrt()方法:
**示例:**这里，8 的立方根被计算为 2，因为当任意 3 次重复时，立方根内部出现任意数字，那么只有一个数字被取出作为立方根的值。
∛8T6 =∛2*2*2T9 = 2

```
Input: Math.cbrt(8)
Output : 2

```

上述方法的更多代码如下:

**程序 1:** Errors and Exceptions，这是一个错误案例，因为找不到复数的立方根，这就是为什么它的参数给出错误。

```
<script type="text/javascript"> 
  // Cube root of complex number can 
  // not be calculated.
  document.write("cbrt of Complex no : " 
                   + Math.cbrt(1 + 2i));
</script> 
```

**输出:**

```
Error: Invalid or unexpected token
```

**程序 2:** 找不到字符串的立方根，这就是函数的字符串参数给出 NaN 即不是数字的原因。只有整数值可以用作函数的参数。

```
<script type="text/javascript"> 
   // Only number can be used as the parameter
   // here string as parameter gives NaN i.e, 
   // not a number.
   document.write("cbrt of a string : " 
                     + Math.cbrt("gfg"));
</script> 
```

**输出:**

```
cbrt of a string: NaN
```

**程序 3:** 每当我们需要得到任意数字的立方根时，我们都会借助 JavaScript 中的 Math.cbrt()函数。

```
<script type="text/javascript"> 
   // Here the Math.cbrt() function 
   // calculates cube root for
   // different numbers taken as 
   // function's parameter.
   document.write("Output : " 
                  + Math.cbrt(125) + "<br>");
   document.write("Output : " 
                  + Math.cbrt(23) + "<br>"); 
</script> 
```

**输出:**

```
Output : 5
Output : 2.8438669798515654
```

**支持的浏览器:**

*   谷歌 Chrome 38.0
*   Internet Explorer 12.0
*   Firefox 25.0
*   Opera 25.0
*   Safari 8.0