# JavaScript Date getDay()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getday-method/](https://www.geeksforgeeks.org/javascript-date-getday-method/)

下面是 **Date getDay()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
    // Here a date has been assigned
    // while creating Date object
    var A = new Date('October 15, 1996 05:35:32');

    // Day of the week from above Date Object is
    // being extracted using getDay()
    var Day = A.getDay();

    // Printing day of the week
    document.write("Number of Day: " +Day);
</script>                   
```

*   **输出:**

```
Number of Day: 2
```

**date.getDay()** 方法用于从给定的 date 对象中获取一周中的某一天(0 到 6)。
**语法:**

```
DateObj.getDay()
```

**参数:**此方法不接受任何参数。
**返回值:**返回给定日期的星期几。一周中的某一天将以整数值的形式返回，从 0 到 6 表示周日为 0，周一为 1，以此类推，直到周六为 6。
上述方法的更多代码如下:
**程序 1:** 如果没有给出月份的日期，默认情况下，函数会将其视为月份的第一个日期，因此会返回星期几。这是一个特例。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // While creating a Date object
  var A = new Date('July 1974');

  var B = A.getDay();

  // Printing day
  document.write("Number of Day: "+B);
</script>                   
```

**输出:**

```
Number of Day: 1
```

**程序 2:** 月份的日期必须在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是一个数字，因为月份的日期不存在。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var A = new Date('October 35, 1996 05:35:32');

  // Day of the week from above Date Object
  // is being extracted using getDay()
  var B = A.getDay();

  // Printing day of the week.
  document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 3:** 如果没有给定参数，则返回当前周的当天。

## java 描述语言

```
<script>
  // Creating Date Object
  var A = new Date();

  // day of the week from above object
  // is being extracted using getDay().
  var B = A.getDay()

  // Printing day of the week.
  document.write(B);
</script>
```

**输出:**

```
5
```

**支持的浏览器:**JavaScript Date getDay()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上