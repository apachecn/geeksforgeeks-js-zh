# JavaScript 数学 LOG2E 属性

> 原文:[https://www . geesforgeks . org/JavaScript-math-log2e-property/](https://www.geeksforgeeks.org/javascript-math-log2e-property/)

下面是**数学 LOG2E** 属性的例子。

*   **例:**

    ```
    <script>
      // Here value of Math.LOG2E is printed.
      document.write(Math.LOG2E);                      
    </script>
    ```

*   **输出:**

    ```
    1.4426950408889634
    ```

数学。LOG2E 是 JavaScript 中的一个属性，简单来说就是用来求 e 的基 2 对数的值，其中 e 是一个约等于 2.718 的无理数和超越数

**语法:**

```
Math.LOG2E;
```

**返回值:**它只是返回 e 的以 2 为底的对数的值。

下面的例子说明了 JavaScript 中的 Math LOG2E 属性。

*   **示例:**这里简单地将 e 的以 2 为底的对数的值显示为输出。

    ```
    Input : Math.LOG2E
    Output:1.4426950408889634
    ```

以上属性的更多代码如下:
**程序 1:**e 的以 2 为底的对数的值可以如下所示的函数形式打印出来。

```
<script>
  // function is being called.
  function get_Value_of_base_2_lagarithm_of_e()
  {
      return Math.LOG2E;
  }

  // function is calling.
  document.write(get_Value_of_base_2_lagarithm_of_e());
</script>
```

**输出:**

```
1.4426950408889634
```

**程序 2:** 这里我们考虑数学。LOG2E 作为一个函数，但实际上它是一个属性，这就是为什么错误作为输出被显示。

```
<script>
  // Here we consider Math.LOG2E as a function but 
  // in actual it  is a property that is why error 
  // as output is being shown.
  document.write(Math.LOG2E(12));
</script>
```

**输出:**

```
Error: Math.LOG2E is not a function
```

**程序 3:** 每当我们需要求 e 的以 2 为底的对数的值时，那时候我们就借助这个性质。在数学中，它需要很多。

```
<script>
  // Value of Math.LOG2E is printed.
  document.write(Math.LOG2E);
</script>
```

**输出:**

```
1.4426950408889634
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队