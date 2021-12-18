# 使用 JavaScript 比较两个日期

> 原文:[https://www . geesforgeks . org/compare-two-date-use-JavaScript/](https://www.geeksforgeeks.org/compare-two-dates-using-javascript/)

在本文中，我们将比较 Javascript 中的两个日期，并通过示例了解它们的实现。

在 JavaScript 中，我们可以通过将两个日期转换成数字值来比较它们，以对应于它们的时间。首先，我们可以使用 [**getTime()**](https://www.geeksforgeeks.org/javascript-date-gettime-method/) 函数将日期转换为数值。通过把给定的日期转换成数值，我们可以直接比较它们。

**示例 1:** 本示例使用 **getTime()** 函数说明日期的比较。

## JavaScript

```
<script>

    // Current Date
    var g1 = new Date();
    var g2 = new Date();
    if (g1.getTime() === g2.getTime())
        document.write("Both  are equal");
    else
        document.write("Not equal");
    javascript: ;
</script>
```

**输出:**

```
Both are equal
```

**示例 2:** 本示例使用 **getTime()** 函数说明当前日期与分配日期的比较。

## Javascript

```
<script>
    var g1 = new Date();

    // (YYYY-MM-DD)
    var g2 = new Date(2019 - 08 - 03);
    if (g1.getTime() < g2.getTime())
        document.write("g1 is lesser than g2");
    else if (g1.getTime() > g2.getTime())
        document.write("g1 is greater than g2");
    else
        document.write("both are equal");
</script>
```

**输出:**

```
g1 is greater than g2
```

**示例 3:** 本示例使用 **getTime()** 函数说明了两个给定日期的比较。

## Javascript

```
<script>
    var g1 = new Date(2019, 08, 03, 11, 45, 55);

    // (YYYY, MM, DD, Hr, Min, Sec)
    var g2 = new Date(2019, 08, 03, 10, 22, 42);
    if (g1.getTime() < g2.getTime())
        document.write("g1 is lesser than g2");
    else if (g1.getTime() > g2.getTime())
        document.write("g1 is greater than g2");
    else
        document.write("both are equal");
</script>
```

**输出:**

```
g1 is greater than g2
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。