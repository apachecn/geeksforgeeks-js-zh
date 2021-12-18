# JavaScript 数学 LN2 属性

> 原文:[https://www.geeksforgeeks.org/javascript-math-ln2-property/](https://www.geeksforgeeks.org/javascript-math-ln2-property/)

下面是**数学 LN2()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here value of Math.LN2 is printed.
  document.write(Math.LN2);                     
</script>
```

*   **输出:**

```
0.6931471805599453
```

数学。LN2 是 JavaScript 中的一个属性，简单来说就是用来求自然对数 2 的值。自然对数以 e 为基数，用 ln 表示。所以，2 的自然对数表示为 ln(2)，其值约为 0.693。
**语法:**

```
Math.LN2;
```

**参数:**此方法不接受任何参数。
**返回值:**它只是返回自然对数的值 2。
下面的例子说明了 JavaScript 中的 Math LN2 属性。

*   **例子:**这里简单的是自然对数 2 的值，即数学。LN2 显示为输出。

```
Input : Math.LN2
Output : 0.6931471805599453
```

以上属性的更多代码如下:
**程序 1:** 自然对数 2 的值可以如下所示的函数形式打印。

## java 描述语言

```
<script>
  // function is being called.
  function get_Value_of_natural_log_of_2()
  {
     return Math.LN2;
  }

  // Calling Function.
  document.write(get_Value_of_natural_log_of_2());
</script>
```

**输出:**

```
0.6931471805599453
```

**程序 2:** 这里我们考虑数学。LN2 作为一个函数，但实际上它是一个属性，这就是为什么误差作为输出被显示。

## java 描述语言

```
<script>
  // Here we consider Math.LN2 as a
  // function but in actual it
  // is a property that is why error as
  // output is being shown.
  document.write(Math.LN2(12));       
</script>
```

**输出:**

```
Error: Math.LN2 is not a function
```

**注意:**检查控制台有无错误。
**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队