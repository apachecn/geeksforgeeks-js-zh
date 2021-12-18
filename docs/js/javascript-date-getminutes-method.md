# JavaScript 日期 getMinutes()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-get minutes-method/](https://www.geeksforgeeks.org/javascript-date-getminutes-method/)

下面是 **Date getMinutes()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 15, 1996 05:35:32');

  // minutes from above DateObj is being
  // extracted using getMinutes().
  var minutes = DateObj.getMinutes();

  // Printing minute.
  document.write(minutes);
</script>
```

*   **输出:**

```
35
```

**date.getMinutes()** 方法用于从给定的 date 对象中获取分钟。
**语法:**

```
DateObj.getMinutes()
```

**参数:**本功能不接受任何参数。
**返回值:**返回给定日期对象的分钟数。分钟是一个从 0 到 59 的整数值。
以上方法的更多代码如下:
**例 1:** 这里月份的日期必须在 1 到 31 之间，因为没有日期的月份大于 31，这就是为什么它返回 NaN，即不是一个数字，因为月份的日期不存在，当月份的日期为 33，即大于 31 时，分钟将不存在。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating a Date object
  var DateObj = new Date('October 35, 1996 05:35:32');

  // minutes from above DateObj is
  // being extracted using getMinutes()
  var minutes = DateObj.getMinutes();

  // Printing minutes
  document.write(minutes);
</script>
```

**输出:**

```
NaN
```

**例 2:** 如果未给出分钟，则返回零(0)。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 12, 1996');

  // minutes from above DateObj is
  // being extracted using getMinutes()
  var minutes = DateObj.getMinutes();

  // Printing minutes
  document.write(minutes);
</script>
```

**输出:**

```
0
```

**例 3:** 如果没有给定参数，则返回当前分钟。

## java 描述语言

```
<script>
  // Creating a date object
  var DateObj = new Date();

  // minutes from above DateObj is
  // being extracted using getMinutes()
  var minute = DateObj.getMinutes();

  // Printing current minute
  document.write(minute);
</script>
```

**输出:**

```
23
```

**支持的浏览器:**JavaScript Date getMinutes()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上