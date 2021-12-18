# JavaScript Date getFullYear()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-get full year-method/](https://www.geeksforgeeks.org/javascript-date-getfullyear-method/)

下面是 **Date getFullYear()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('October 15, 1996 05:35:32');

  // year from above date object is
  // being fetched using getFullYear().
  var B = dateobj.getFullYear();

  // Printing year
  document.write(B);
</script>
```

*   **输出:**

```
1996
```

方法用于从给定的日期对象中获取年份。
**语法:**

```
DateObj.getFullYear()
```

**参数:**此功能不接受任何参数。
**返回值:**返回给定日期的年份。
以上方法的更多代码如下:
**程序 1:** 如果没有给 Date()构造函数任何参数，那么 **getFullYear()** 函数返回当前年份。

## java 描述语言

```
<script>
  // Creating Date Object
  var dateobj = new Date();

  // year from above object
  // is being fetched using getFullYear().
  var B = dateobj.getFullYear();

  // Printing current year
  document.write(B);
</script>
```

**输出:**

```
2018
```

**程序 2:** 一个月的日期必须在 1 到 31 之间，因为一个月不能超过 31 天。这就是为什么它返回 NaN，即不是一个数字，因为月份的日期不存在。因此，当月份日期设置为 45 或任何不在 1 到 31 之间的数字时，年份将不存在。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('October 45, 1996 05:35:32');

  // year from above date object is
  // being fetched using getFullYear().
  var B = dateobj.getFullYear();

  // Printing year
  document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 3:** 有获取当年等应用。它在网站中用于验证用户的年龄。

## java 描述语言

```
<script>
  // Creating Date Object
  var dateobj = new Date();

  // Year from above object
  // is being fetched using getFullYear()
  var B = dateobj.getFullYear();

  // Printing current year
  document.write(B);
</script>
```

**输出:**

```
2018
```

**支持的浏览器:**以下列出 **JavaScript Date getFullYear()方法**支持的浏览器:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上