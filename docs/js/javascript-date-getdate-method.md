# JavaScript Date getDate()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-get date-method/](https://www.geeksforgeeks.org/javascript-date-getdate-method/)

下面是 **Date getDate()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('October 13, 1996 05:35:32');

  // date of the month from above Date Object is
  // being extracted using getDate()
  var B = dateobj.getDate();

  // Printing date of the month
  document.write(B);
</script>
```

*   **输出:**

```
13
```

**date.getdate()** 方法用于从给定的 Date 对象中获取一个月的日期。
**语法:**

```
DateObj.getDate()
```

**参数:**该方法不取任何参数。它只是和一个日期对象一起使用，我们想从中获取月份的日期。
**返回值:**返回给定日期的月份日期。月份日期是一个从 1 到 31 的整数值。
**注意:****DateObj**是使用 Date()constructor 创建的有效日期对象，我们希望从中获取日期。
上述方法的更多代码如下:
**示例 1:** 月份的日期必须在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('October 33, 1996 05:35:32');

  // date of the month given above date object
  // is being extracted using getDate().
  var B = dateobj.getDate();

  // Printing date of the month.
  document.write(B);
</script>
```

**输出:**

```
NaN
```

**例 2:** 如果没有给出月份日期，默认返回 1。这是个例外。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('October 1996 05:35:32');

  // date of the month from above date object
  // is extracted using getDate()
  var B = dateobj.getDate();

  // Printing date of the month
  document.write(B);
</script>
```

**输出:**

```
1
```

**例 3:** 如果没有给 Date 构造函数任何参数，那么函数返回当月的当前日期。

## java 描述语言

```
<script>
  // Creating Date Object
  var dateobj = new Date();

  // date of the month from above object
  // is being extracted using getDate().
  var B = dateobj.getDate();

  // Printing current date
  document.write(B);
</script>
```

**输出:**

```
21
```

**支持的浏览器:**JavaScript Date getDate()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上