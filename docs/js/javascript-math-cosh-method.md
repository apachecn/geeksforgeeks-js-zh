# JavaScript 数学 cosh()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-cosh-method/](https://www.geeksforgeeks.org/javascript-math-cosh-method/)

下面是数学方法的例子。

*   **示例:**

## java 描述语言

```
<script>
  // Printing hyperbolic cosine of some numbers
  // taken as parameter of Math.cosh() method.
  document.write(Math.cosh(0) + "<br>");
  document.write(Math.cosh(1) + "<br>");
  document.write(Math.cosh(0) + "<br>");
  document.write(Math.cosh(22) + "<br>");
  document.write(Math.cosh(-2) + "<br>");
  document.write(Math.cosh(4));
</script>
```

*   **输出:**

```
 1
 1.5430806348152437
 1
 1792456423.065796
 3.7621956910836314
 27.308232836016487
```

**Math.cosh()** 方法用于计算一个数的双曲余弦值。

**语法:**

```
Math.cosh(x)
```

**参数:** 该方法接受如上所述的单个参数，描述如下:

*   **x:** 此参数保存一个将要计算双曲余弦值的数字。
    **返回:** 返回该数的双曲余弦的计算值。
    下面的例子说明了 JavaScript 中的 Math cosh()方法:

*   **例 1:** 这里计算任意数的双曲余弦的公式为:数 **e** 是一个数学常数，其近似值等于 **2.718** 。

> ![ \frac{e^{p} + e^{-p}}{2} = \frac{e^{0} + e^{-0}}{2}=\frac{1+1}{2}= 1  ](img/87ac28981a91916a0dc4b3876fc2c485.png)

```
Input : Math.cosh(0)
Output : 1
```

*   **例 2:** 同样，只要用所需的数代替 p，就可以计算出任意数的双曲余弦。这里与上面的计算相同，当我们放 12 而不是 p 时，该值变成如上所示的输出。

```
Input : Math.cosh(12)
Output : 81377.39571257407
```

以上方法的更多代码如下:

**程序 1:** Errors and Exceptions，它是一个错误案例因为复数不能作为方法的参数只有整数值可以作为参数。

## java 描述语言

```
<script>
  // Complex number can not be calculated as the
  // hyperbolic cosine.
  document.write(Math.cosh(1 + 2i));
</script>
```

**输出:**

```
Error: Invalid or unexpected token
```

**程序 2:** 除了整数之外，没有任何东西被接受作为方法的参数，这就是为什么这里——字符串作为参数给出 NaN，即不是数字。

## java 描述语言

```
<script>
  // Any string value as the parameter of the method
  // gives NaN i.e, not a number
  // because only number can be used as the parameters.
  document.write(Math.cosh("geeksforgeeks") + "<br>");
  document.write(Math.cosh("gfg"));                   
</script>
```

**输出:**

```
NaN
NaN
```

**程序 3:** 它的实际应用是，每当我们需要求一个数的双曲余弦值的时候，我们就借助 JavaScript 中的 Math.cosh()方法。

## java 描述语言

```
<script>
  // Printing hyperbolic cosine of some numbers
  // from 0 to 9 taken as parameter
  for (i = 0; i < 10; i++) {
      document.write(Math.cosh(i) + "<br>");
  }
</script>
```

**输出:**

```
1
1.5430806348152437
3.7621956910836314
10.067661995777765
27.308232836016487
74.20994852478785
201.7156361224559
548.317035155212
1490.479161252178
4051.5420254925943
```

**支持的浏览器:**

*   谷歌 Chrome 38.0
*   Internet Explorer 12.0
*   Firefox 25.0
*   Opera 25.0
*   Safari 8.0