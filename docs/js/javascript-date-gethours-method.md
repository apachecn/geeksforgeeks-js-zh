# JavaScript 日期 getHours()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-get hours-method/](https://www.geeksforgeeks.org/javascript-date-gethours-method/)

下面是 **Date getHours()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var A = new Date('October 15, 1996 05:35:32');

  // hour from above is being
  // extracted using getHours()
  var B = A.getHours();

  // Printing hour.
  document.write(B);
</script>
```

*   **输出:**

```
5
```

**date.getHours()** 方法用于从给定的 date 对象返回小时。
**语法:**

```
DateObject.getHours()
```

**参数:**此方法不接受任何参数。
**返回值:**返回给定日期对象的小时数。Hours 是一个介于 0 到 23 之间的整数值。
以上方法的更多代码如下:
**程序 1:** 如果没有给出小时，则返回零(0)。这是个例外。

## java 描述语言

```
<script>
  // Creating a Date object
  var A = new Date('October 12, 1996');

  // extracting hours from the date object
  var B = A.getHours();

  // Printing hour.
  document.write(B);
</script>
```

**输出:**

```
0
```

**程序 2:** 这里月份的日期必须在 1 到 31 之间，因为没有日期可以有大于 31 的月份。这就是为什么如果 Date 对象中的月份大于 31，它会返回 NaN，即 Not Number。当给出的月份日期为 33，即大于 31 时，小时数将不存在。

## java 描述语言

```
<script>
  // Creating a Date object
  var A = new Date('October 35, 1996 12:35:32');

  var B = A.getHours();

  // Printing hour.
  document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 3:** 如果没有给定参数，则返回当前小时数。

## java 描述语言

```
<script>
  // Creating a Date object
  var A = new Date();

  var B = A.getHours();

  // Printing present hour.
  document.write(B);
</script>
```

**输出:**

```
15
```

**支持的浏览器:**JavaScript Date getHours()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上