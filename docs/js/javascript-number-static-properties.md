# JavaScript 数字静态属性

> 原文:[https://www . geesforgeks . org/JavaScript-number-static-properties/](https://www.geeksforgeeks.org/javascript-number-static-properties/)

JavaScript Number 是一个可以表示诸如整数、浮点、十六进制、十进制等数值的对象。它充当原始数值的包装对象。它有各种方法和属性，用于对数字执行不同的任务。下表显示了 Number 对象的一些静态属性，这些属性可以作为常数在整个程序中使用。

**属性:**

*   **MAX_VALUE:** 返回 JavaScript 支持的最大数值。
*   **MIN_VALUE:** 返回最接近 0 的最小正数值，但不是最大负数。
*   **NEGATIVE_INFINITY:** 表示负无穷大值。
*   **POSITIVE_INFINITY:** 表示正无穷大值。
*   **MIN_SAFE_INTEGER:** 表示 JavaScript 中的最小安全整数。
*   **NaN:** 用于表示非合法数字的值。

以下示例演示了如何使用数字的这些属性。

**示例 1:** 在这个示例中，我们找出了 JavaScript 中支持的最大值和最小值。

## 超文本标记语言

```
<html>
<body>
  <h1>
    Number properties max value
    and min value
  </h1>
  <script>
    console.log('Maximum Value:',
                Number.MAX_VALUE);
    console.log('Minimum Value:',
                Number.MIN_VALUE);
  </script>
</body>
</html>
```

**控制台输出:**

```
Maximum Value: 1.7976931348623157e+308
Minimum Value: 5e-324
```

**例 2:** 在这个例子中，我们找出了 JavaScript 中的正无穷大和负无穷大的值。

## 超文本标记语言

```
<html>
<body>
  <h1>
    Number properties negative
    infinity and positive infinity
  </h1>
  <script>
    console.log('Negative Infinity:',
                Number.NEGATIVE_INFINITY);
    console.log('Positive Infinity:',
                Number.POSITIVE_INFINITY);
  </script>
</body>
</html>
```

**控制台输出:**

```
Negative Infinity: -Infinity
Positive Infinity: Infinity
```