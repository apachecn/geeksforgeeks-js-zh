# JavaScript 数学 LN10 属性

> 原文:[https://www . geesforgeks . org/JavaScript-math-ln10-property/](https://www.geeksforgeeks.org/javascript-math-ln10-property/)

以下是**数学 LN10()** 属性的示例。

*   **例:**

    ```
    <script>
      // Here value of Math.LN10 is printed.
      document.write(Math.LN10);                      
    </script>
    ```

*   **输出:**

    ```
    2.302585092994046
    ```

数学。LN10 是 JavaScript 中的一个属性，简单来说就是用来求自然对数 10 的值。自然对数以 e 为基数，用 ln 表示。因此，10 的自然对数表示为 ln(10)，其值约为 2.302

**语法:**

```
Math.LN10;
```

**返回值:**简单的返回自然对数的值 2。

下面的例子说明了 JavaScript 中的数学 LN10 属性。

**例子:**这里简单的是自然对数 2 的值，即数学。LN10 显示为输出。

```
Input : Math.LN10
Output : 2.302585092994046
```

以上属性的更多代码如下:
**程序 1:** 自然对数 2 的值可以如下所示的函数形式打印。

```
<script>
  // function is being called.
  function get_Value_of_natural_log_of_10()
  {
     return Math.LN10;
  }

  // Calling Function.
  document.write(get_Value_of_natural_log_of_10());
</script>
```

**输出:**

```
2.302585092994046
```

**程序 2:** 这里我们考虑数学。LN10 作为一个函数，但实际上它是一个属性，这就是为什么误差作为输出被显示。

```
<script>
  // Here we consider Math.LN10 as a 
  // function but in actual it
  // is a property that is why error as
  // output is being shown.
  document.write(Math.LN10(12));        
</script>
```

**输出:**

```
Error: Math.LN10 is not a function
```

**注意:**检查控制台有无错误。

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队